# Modelos de inferência

Este documento reúne as fichas dos modelos que rodam no serviço de inferência da Rede Cívica. Ele complementa a [Política de IA](AI_POLICY.md) e a [referência pública de modelos](https://docs.redecivica.com.br/referencia-modelos-de-inferencia/). O serviço não decide. Ele devolve modelo, revisão, confiança e duração. Limiar, decisão, moderação e prioridade ficam na API.

As revisões abaixo são as que estão pinadas em `app/motores/revisoes.py`, no repositório do serviço. Nenhuma célula de licença ou revisão fica vazia. A troca de modelo ou de revisão segue o processo descrito em [Versionamento](#versionamento).

## Fichas

| Capacidade | Modelo | Revisão | Licença | Fonte | Runtime | Hardware | Limites | Uso comercial | Atribuição |
|---|---|---|---|---|---|---|---|---|---|
| Imagem, descrição | `onnx-community/Florence-2-base` | `d59e079711c57174f29265539fb4cc9f0f335916` | MIT | [Model card](https://huggingface.co/onnx-community/Florence-2-base) | ONNX Runtime | CPU; 2 threads intra e 1 inter; pesos q8 no volume; 1,6 s por inferência quente | Legenda em inglês; confiança nula; falha por imagem | Permitido | [Microsoft](#atribuição) |
| Imagem, classificação NSFW | `AdamCodd/vit-base-nsfw-detector` | `8587de998f441aac03fdd57a85d2e4cb808c7d64` | Apache-2.0 | [Model card](https://huggingface.co/AdamCodd/vit-base-nsfw-detector) | ONNX Runtime | CPU; 2 threads intra e 1 inter; 85 MB em disco; 100 MB residente; 1,5 s | Score bruto; limiar na API; não decide | Permitido | [AdamCodd](#atribuição) |
| Imagem, detecção de pessoa | `skillsafe-ai/detr-resnet-50` | `72bdf30a61874a22deecf48c732e120c11bc1a4a` | Apache-2.0 | [Model card](https://huggingface.co/skillsafe-ai/detr-resnet-50) | ONNX Runtime | CPU; 2 threads intra e 1 inter; 42 MB em disco; 50 MB residente | Só presença de pessoa; sem reconhecimento facial; score bruto | Permitido | [Skillsafe AI e Meta](#atribuição) |
| Áudio, transcrição | `Systran/faster-whisper-tiny` | `d90ca5fe260221311c53c58e660288d3deb8d356` | MIT | [Model card](https://huggingface.co/Systran/faster-whisper-tiny) | faster-whisper e CTranslate2 int8 | CPU; 2 threads e 1 worker; 72 MB de pesos; cerca de 1x o tempo real; 0,3 s quente | Confiança nula; ruído, sotaque e fala sobreposta; revisão obrigatória | Permitido | [OpenAI e Systran](#atribuição) |
| Tradução | `ooeoeo/opus-mt-tc-big-en-pt-ct2-float16` | `1b42ae200c9d9149b316a043b0b56874abcd62f8` | CC BY 4.0 | [Model card da conversão](https://huggingface.co/ooeoeo/opus-mt-tc-big-en-pt-ct2-float16) e [modelo de origem](https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-en-pt) | CTranslate2 int8 | CPU; 2 threads intra e 1 inter; 446 MB de pesos; 0,06 a 0,1 s quente | Só en→pt; falha mantém a legenda original | Permitido com atribuição | [Helsinki-NLP e ooeoeo](#atribuição) |
| Texto | `Qwen/Qwen2.5-1.5B-Instruct-GGUF` | `91cad51170dc346986eccefdc2dd33a9da36ead9` | Apache-2.0 | [Model card](https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct-GGUF) | llama.cpp com llama-cpp-python | CPU; 2 threads; 1,12 GB de pesos; contexto de 4096; 9 a 23 s para 2 a 10 legendas | Pode alucinar; saída validada e descartada por item; não decide | Permitido | [Alibaba Qwen](#atribuição) |

O LanguageTool 6.8 não é um modelo de aprendizado. Ele é um motor de regras e aparece em [O que não é modelo](#o-que-não-é-modelo).

## Hardware e modos

O serviço roda em CPU e RAM. A VPS atual não tem placa de vídeo. A variante com GPU está prevista como repositório próprio, com o mesmo contrato `/v1`.

O cenário de 8 GB usa 5 GB e 3,5 vCPU para o serviço, com as cinco capacidades residentes, e 1,5 GB de memória e 1,5 vCPU para a API. O pico medido com tudo carregado é de 3,31 GiB. O serviço ocioso, sem modelo carregado, consome cerca de 137 MB.

O cenário de 4 GB fica como rollback. O serviço usa 3,4 GB e 1,5 vCPU e mantém descrição, classificação e tradução residentes, com pico medido de 2,69 GiB. A API usa 1 GB e 1,5 vCPU. O cenário de 4 GB não comporta as cinco capacidades residentes.

O modo local executa os modelos no processo da API. Ele cobre imagem, áudio e tradução. A capacidade de texto roda só no serviço. A API usa 3 GB e 1,5 vCPU no cenário de 4 GB, com `q8` e a tradução desligada. O rollback do modo HTTP é `INFERENCIA_MODO=local` com redeploy da API.

O carregamento é preguiçoso e residente. Um processo e um worker por container. Vários workers duplicariam os pesos na RAM e ficam proibidos.

As threads são medidas, não arbitradas. O ONNX Runtime usa 2 threads intra e 1 inter por sessão. O CTranslate2 usa 2 intra e 1 inter. O Whisper usa 2 threads de CPU e 1 trabalhador. O llama.cpp usa `INFERENCIA_THREADS_TEXTO`, com 2 no valor medido. O teto não sobe sem nova medição.

### Modo sem IA

O modo sem IA é operacional, não um build separado. Cada capacidade tem uma válvula. Com a válvula desligada, a rota responde 503 e o cliente degrada. Com todas desligadas, nenhum modelo é carregado e o serviço fica ocioso. A API mantém o fluxo determinístico.

No serviço, as válvulas são `INFERENCIA_DESCRICAO_HABILITADA`, `INFERENCIA_CLASSIFICACAO_HABILITADA`, `INFERENCIA_TRANSCRICAO_HABILITADA`, `INFERENCIA_TRADUCAO_HABILITADA` e `INFERENCIA_TEXTO_HABILITADO`. No modo local, as válvulas equivalentes são `D1B_*` e `D1C_*`.

Os textos assistidos nascem desligados. `TEXTOS_ASSISTIDOS_HABILITADO` e `TRIAGEM_ASSISTIDA_HABILITADA` deixam os campos nulos no modo local e não bloqueiam projeção, fila ou leitura.

## Versionamento

Cada motor do serviço declara a revisão do Hugging Face pinada pelo identificador do commit em `app/motores/revisoes.py`. O contrato devolve `modelo` e `versao_modelo`.

Não há tag flutuante no serviço. `latest`, `main` e equivalentes não entram na produção. A troca de revisão é uma mudança de modelo. Exige atualização do registro, dos testes de paridade ou do corpus e desta ficha.

Os prompts também têm versão. A consolidação usa `consolidar_v1`. O resumo assistido usa `jornada_v1`, `dossie_v1`, `agregado_v1` e `triagem_v1`. O cache do texto assistido usa o hash das entradas mais a versão do prompt e a revisão do modelo.

O modo local do Node é o caminho de rollback para imagem, áudio e tradução, com as mesmas famílias de modelo. A capacidade de texto roda só no serviço. A tabela canônica de produção é a do serviço, com revisão pinada.

A versão do contrato é `1.0.0`. Mudança de modelo não eleva a versão. Mudança incompatível de rota, campo ou código de erro sobe para `/v2` e incrementa o campo `contrato`.

## Limites e falhas

Nenhum modelo decide. Limiar, moderação, prioridade, publicação e remoção ficam na API. Não há reconhecimento facial. A detecção de pessoa apenas sinaliza presença.

O projeto não envia conteúdo do cidadão a serviço externo de inferência. A comunicação com o Hugging Face acontece no primeiro uso de cada modelo, apenas para baixar os pesos.

O texto pode alucinar. Cada frase da consolidação e cada saída de resumo é validada antes de sair do serviço. O item inválido é descartado e os válidos permanecem. O texto assistido é aditivo e nunca substitui o template determinístico.

| Capacidade | Falha, fila cheia ou tempo limite | Efeito |
|---|---|---|
| Transcrição | Motor indisponível ou acima do tempo | A demanda segue sem o texto e a confiança é penalizada. |
| Descrição | Motor indisponível ou acima do tempo | A imagem fica sem descrição e as demais continuam. |
| Tradução | Motor indisponível ou acima do tempo | A legenda original é mantida. |
| Consolidação | Falha, 429, 503 ou 504 | O resumo por imagem não é composto. As legendas individuais permanecem. |
| Texto assistido | Falha, saída inválida, 429, 503 ou 504 | O campo fica nulo. O estruturado determinístico continua visível. |
| Classificação | Válvula desligada | A heurística de documento e PII decide. |
| Classificação | Capacidade habilitada e serviço indisponível | A imagem vai para a fila humana. Imagem sem classificação não entra na projeção pública. |
| Assistência de texto | LanguageTool indisponível | A resposta é `disponivel: false` e o envio do formulário segue normal. |

## Uso comercial e licenças

Nenhum modelo desta tabela restringe uso comercial. As licenças exigem atribuição e, quando for o caso, a reprodução do aviso.

| Licença | Regra |
|---|---|
| MIT | Uso comercial permitido, com o aviso de copyright e a licença. |
| Apache-2.0 | Uso comercial permitido, com o aviso, a licença e a indicação de alterações. |
| CC BY 4.0 | Uso comercial permitido, com atribuição, link para a licença e indicação de alterações. |
| LGPL-2.1 | LanguageTool. Uso permitido, com as obrigações da LGPL-2.1 para o componente, que roda em container próprio. |

A conversão CTranslate2 do OPUS-MT registra Apache-2.0 na própria model card. O modelo de origem, `Helsinki-NLP/opus-mt-tc-big-en-pt`, declara CC BY 4.0. A conversão não muda a licença dos pesos. O projeto registra CC BY 4.0, atribui Helsinki-NLP e a conversão de ooeoeo e mantém a atribuição exigida pela origem.

O serviço é AGPL-3.0. As licenças dos modelos não mudam a licença do serviço. A distribuição oficial do código continua AGPL-3.0.

## Atribuição

A coluna Atribuição da tabela nomeia o titular. A lista completa, com bibliotecas e dados, está na [referência de licenças e atribuições](https://docs.redecivica.com.br/referencia-modelos-de-inferencia/#licenças-e-atribuições). O `THIRD-PARTY-NOTICES.md` do repositório `mvp-inferencia` traz a mesma lista e é publicado com o repositório.

| Componente | Atribuição |
|---|---|
| Florence-2 base | Microsoft. |
| Classificador NSFW | AdamCodd. |
| Detecção de pessoa | Skillsafe AI e Meta (DETR). Export ONNX de Xenova. |
| Whisper tiny | OpenAI e Systran (conversão para CTranslate2). |
| OPUS-MT en→pt | Helsinki-NLP e ooeoeo (conversão para CTranslate2). |
| Qwen2.5-1.5B-Instruct | Alibaba Qwen. |
| LanguageTool | LanguageTooler GmbH e contribuidores. |

As conversões ONNX e CTranslate2 mantêm a licença e a atribuição dos pesos de origem. Dependência ou modelo de terceiro novo entra no `THIRD-PARTY-NOTICES.md` do repositório que o carrega.

## Feedback de modelo

Erro, viés, falso positivo, falso negativo, resumo alucinado, erro de transcrição, erro de tradução ou comportamento estranho de modelo vai para a categoria Feedback de modelo nas [Discussões](https://github.com/Rede-Civica/.github/discussions). A regra está na [Política de IA](AI_POLICY.md#feedback-de-modelo).

Inclua:

- tarefa do modelo;
- modelo e versão, se souber;
- data e tela ou endpoint;
- resultado esperado;
- resultado observado;
- impacto;
- se houve revisão humana;
- evidência de teste, quando possível.

Não inclua dado pessoal, mídia real de terceiros, credencial, token ou conteúdo confidencial. Use dados de teste. Se o caso exigir dado sensível, diga isso sem enviar o dado e peça um canal privado.

A primeira resposta humana sai em até 2 dias úteis. A triagem pode abrir uma issue ou uma correção. A decisão fica registrada no tópico. Não há garantia nem prazo para correção.

Vulnerabilidade de segurança vai para o [SECURITY.md](SECURITY.md). Conduta vai para o [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Bug de produto que não é de modelo vai para o formulário de issue.

## O que não é modelo

O LanguageTool é um motor de regras, não um modelo de aprendizado. Ele revisa ortografia e gramática, roda em container próprio e usa a licença LGPL-2.1.

Também não são modelos de inferência: a heurística de documento e PII, a denylist de termos, a categorização por dicionário, a similaridade textual da detecção de duplicidade, a sugestão de estruturação da relatoria e os conjuntos de dados do mapa. Esses mecanismos ficam nas trilhas próprias e não entram nesta ficha.

## Referências

- [Modelos de inferência: como funcionam](https://docs.redecivica.com.br/modelos-de-inferencia/)
- [Referência de modelos de inferência](https://docs.redecivica.com.br/referencia-modelos-de-inferencia/)
- [Referência do deploy](https://docs.redecivica.com.br/referencia-do-deploy/)
- [Política de IA](AI_POLICY.md)
- [Dados da Rede Cívica](DATA.md)
- [Segurança da informação](SECURITY.md)
