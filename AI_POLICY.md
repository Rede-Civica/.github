# Política de uso de IA

Esta política define como a Rede Cívica usa IA e como quem contribui declara o uso. Ela vale para código, documentação, issues, pull requests, revisões, Discussões, reuniões, moderação e produto.

A política não substitui o [código de conduta](CODE_OF_CONDUCT.md), o [plano de segurança da comunidade](COMMUNITY_SAFETY.md), a [política de segurança](SECURITY.md), o [CLA](CLA.md) nem as licenças. Em conflito, valem o código de conduta e a lei. Em segurança, vale a regra mais restritiva.

## Escopo

A política vale para fundador, owners (proprietários), mantenedores, revisores, triagers (organizadores de issues), moderadores, contribuidores, participantes do beta, pessoas convidadas e visitantes.

Ela cobre:

- código, testes, documentação, design e tradução;
- issues, pull requests, revisões e Discussões;
- reuniões, encontros e gravações;
- moderação de conteúdo e de comunidade;
- inferência no produto.

O uso de IA fora dos espaços do projeto não é alcançado pela política. Quando a contribuição entra no projeto, a política vale para ela.

## Princípios

1. **IA reduz atrito.** Ela transcreve, descreve, traduz, resume, classifica e organiza. Não decide, não prioriza, não modera e não substitui a decisão humana.
2. **Output (saída) automático é marcado, versionado e rastreável.** O conteúdo bruto é preservado. A pessoa consegue ver o que foi gerado, por qual modelo e com qual versão.
3. **A pessoa humana responde.** Quem envia, revisa ou aprova responde pelo conteúdo, com ou sem assistência de ferramenta.
4. **Uso de IA é opcional.** A política não cria teste de lealdade tecnológica. Quem não usa IA tem o mesmo direito de contribuir, revisar e progredir na escada.
5. **A contribuição é julgada pelo conteúdo.** O critério é o problema, o critério de aceite, os testes e a revisão. O uso ou não uso de IA não é mérito nem demérito.
6. **Declarar não é pedir permissão.** A declaração informa o uso. A revisão decide se a contribuição entra.
7. **Não há lavagem de licença.** Obra de terceiros mantém licença, atribuição e permissão.
8. **Agente autônomo não abre, revisa, aprova nem mergeia pull request.**
9. **Moderação com IA é assistiva.** A decisão é humana e tem apelação humana.

## Domínios e regras

| Domínio | Permitido | Declaração | Responsável |
|---|---|---|---|
| Código | Sim, com revisão humana e testes | Sim, no pull request | Pessoa que assina o CLA |
| Documentação e texto | Sim, com revisão humana e checagem de fontes | Sim, no pull request ou na issue | Autor |
| Issues, discussões e revisões | Rascunho e resumo sim. Decisão e aprovação não. | Sim, quando a IA produziu parte relevante | Pessoa que publica |
| Moderação | Assistiva, com apelação humana | Interna, marcada no item | Moderador humano |
| Reuniões e anotador | Só com consentimento | Sim, no início e nas notas | Organizador |
| Agentes autônomos | Não abrem, revisam, aprovam nem mergeiam pull request | Não se aplica | Mantenedor que supervisiona a automação |
| Produto | Inferência com marcação, versão e contestação | Na interface e nos metadados | API, web e serviço de inferência |

## Declaração de uso de IA

Declare o uso de IA generativa em código, texto, teste, imagem, áudio, tradução, revisão ou análise. A declaração informa a ferramenta, as partes assistidas e o que foi revisado por uma pessoa.

- Em pull request, use o campo "Uso de IA" do template.
- Em issue ou discussão, escreva a declaração no início do texto.
- Em revisão, diga se a IA ajudou a analisar o diff ou a redigir o comentário.
- Se não usou, escreva "Não usei".

Corretor ortográfico, autocomplete de linha e ferramenta de formatação não exigem declaração separada. Eles não transferem responsabilidade. Se a ferramenta gerou parte relevante do conteúdo, declare.

Declarar não garante aceitação. A contribuição segue os mesmos gates, a mesma revisão e o mesmo critério de qualidade.

## Responsabilidade humana

A pessoa que assina o CLA é a autora de registro e responde pelo conteúdo. A pessoa que revisa responde pelo que aprova. A ferramenta de IA não assina o CLA, não tem direito autoral, não responde e não recebe crédito.

Se o output da IA estiver errado, incompleto, enviesado ou sem licença, a pessoa corrige ou retira. "O modelo escreveu" não é justificativa.

O projeto pode pedir evidência de origem, teste ou revisão humana. Pode recusar conteúdo que não consegue verificar.

## Direito de contribuir

Usar IA é opcional. Ninguém é obrigado a usar IA para contribuir, revisar ou participar. Ninguém é barrado por escolher não usar IA.

O uso de IA não é teste de lealdade. O projeto julga a contribuição, não a ferramenta.

Quem usa IA segue esta política. Quem não usa tem o mesmo direito de contribuir, revisar e subir na escada.

O projeto pode limitar o escopo da primeira contribuição ou pedir um pull request menor. O limite vale para todas as contribuições, com ou sem IA.

## Agentes autônomos e automação

Agente autônomo é o sistema que abre, comenta, revisa, aprova ou mergeia sem uma pessoa decidir no momento da ação.

Agentes podem rascunhar código, texto, teste, resumo e sugestão. Uma pessoa revisa, decide e envia.

Agentes não abrem pull request, não aprovam, não mergeiam, não assinam o CLA e não participam de decisão de governança. Pull request aberto por agente é fechado com indicação desta política. A pessoa responsável pode reenviar o trabalho com autoria humana e declaração de uso.

Automação de rotina é permitida sob responsabilidade do mantenedor: labels, lembretes, atualização de dependência, varredura de segurança, verificação de link e tarefa de release. O mantenedor que configura a automação responde por ela.

Automação que comenta como se fosse pessoa ou esconde a própria natureza é proibida.

## Licença, origem e proveniência

O código do projeto é AGPL-3.0. O texto é CC BY-SA 4.0. Esta política não muda as licenças.

Lavagem de licença (license laundering) é proibida. Isso inclui usar IA para reescrever, parafrasear ou disfarçar código, texto, imagem ou dado de terceiros para escapar de licença, atribuição ou permissão.

Declare a origem e a licença de conteúdo de terceiros. Mantenha a atribuição exigida pela licença.

Output de IA não pode reproduzir conteúdo de terceiros sem permissão. Na dúvida, não inclua.

O CLA cobre a contribuição. Quem contribui declara ter o direito de enviar o conteúdo. A ferramenta de IA não muda esse direito.

No produto, a proveniência registra modelo, versão do modelo, versão do prompt (instrução enviada ao modelo) quando houver, confiança quando aplicável e referência ao conteúdo bruto. A referência pública é [Modelos de inferência](https://docs.redecivica.com.br/modelos-de-inferencia/).

## Pull request em massa

Abra uma issue antes de pull request substantivo. Use um pull request por issue, com escopo claro.

Não abra pull request em massa, refatoração ampla ou mudança gerada em muitos arquivos sem alinhamento prévio.

Pull request assistido por IA segue a mesma regra. Volume não é vantagem.

A primeira contribuição deve ser pequena. Use uma tarefa com o label `good first issue` quando houver.

## Texto legal, conceitual e de governança

IA pode rascunhar, resumir e sugerir. Uma pessoa revisa contra o livro, o SDS, a lei e as fontes.

Texto legal, conceitual e de governança exige revisão humana antes da publicação. IA não é autora única de política, código de conduta, plano de segurança ou texto de licença.

Mudança de governança segue [GOVERNANCE.md](GOVERNANCE.md). Mudança substantiva exige proposta pública de mudança (RFC). O output de IA não substitui a RFC.

O livro é a fonte da verdade. Output de IA que contradiz o livro é corrigido ou descartado.

## Moderação assistida e apelação

IA pode sinalizar, pontuar, classificar, resumir e organizar a fila de moderação. Ela não decide.

- A classificação NSFW bloqueia por limiar e envia para revisão humana.
- A detecção de pessoa apenas sinaliza. Não há reconhecimento facial.
- A denylist de texto apenas sinaliza.
- A triagem assistida resume o item e o histórico. É interna, marcada como gerada por IA e restrita ao card da moderação.

A categorização automática acima do limiar pode publicar o conteúdo com marcação automática e caminho de contestação imediato. Essa publicação é provisória, não é decisão final. Abaixo do limiar, a publicação aguarda revisão humana. Conteúdo sensível, moderação, prioridade, bloqueio e remoção sempre exigem decisão humana.

Cada decisão é registrada em histórico append-only (registro que só recebe novas entradas, sem apagar as anteriores), com decisão, motivo, moderador, data, modelo e versão da assistência quando houver e reversão. O registro não expõe dado pessoal.

A apelação é feita a uma pessoa que não participou da decisão. O pedido vai para `contato@redecivica.com.br`, com o assunto `Moderação de conteúdo`. A primeira resposta humana sai em até 2 dias úteis. A decisão é justificada. Não há garantia de reversão.

Caso de conduta segue [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) e [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md). Vulnerabilidade de segurança segue [SECURITY.md](SECURITY.md).

## Reuniões, gravações e anotador

Gravação, transcrição e anotador automático só acontecem com consentimento de quem participa. O organizador avisa no início, permite recusa e não grava quem pediu para não gravar.

A nota automática é marcada como gerada por IA, revisada antes de publicar e não inclui dado pessoal, conversa privada ou conteúdo de terceiros.

A gravação fica restrita, com prazo de retenção definido, e é apagada quando a pessoa pede, quando possível.

Resumo automático de reunião não substitui a ata aprovada por quem organiza.

## Produto e inferência

A IA no produto é assistiva. Ela transcreve, descreve, traduz, resume, classifica e organiza. Não decide prioridade, moderação, publicação de conteúdo sensível ou alocação de recurso.

Todo output é marcado na interface e nos dados que acompanham a resposta. O conteúdo original permanece disponível. O output é versionado com modelo, revisão, versão do prompt e confiança quando aplicável.

O caminho de contestação é visível. Na categorização, a pessoa contesta e uma pessoa revisa. Na moderação de conteúdo, a apelação vai para uma pessoa.

Não há reconhecimento facial. A detecção de pessoa apenas sinaliza presença. Nenhuma IA identifica pessoas.

Licença de modelo e de base de dados entra no `THIRD-PARTY-NOTICES.md` de cada repositório. A referência pública é a página [Modelos de inferência](https://docs.redecivica.com.br/modelos-de-inferencia/).

Mudança de modelo, prompt ou limiar segue a revisão e a sincronização de parâmetros. Parâmetro público permanece nos dois espelhos: o Apêndice C do livro e `public-parameters.json` do web.

## Feedback de modelo

Use a categoria Feedback de modelo nas [Discussões](https://github.com/Rede-Civica/.github/discussions) para relatar falso positivo, falso negativo, resumo alucinado, viés, erro de classificação, erro de transcrição, erro de tradução ou outro comportamento de modelo.

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

Vulnerabilidade de segurança vai para [SECURITY.md](SECURITY.md). Conduta vai para [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Bug de produto que não é de modelo vai para o template de issue.

## Governança desta política

O fundador e os mantenedores respondem pela política. A revisão acontece pelo menos uma vez por ano, quando um modelo ou domínio novo entra ou quando um incidente mostra lacuna.

Mudança substantiva segue [GOVERNANCE.md](GOVERNANCE.md) e exige proposta pública de mudança (RFC), com 14 dias de comentários para mudança substantiva e 30 dias para mudança de princípio. Correção editorial pode entrar por pull request direto.

A política é revisada por pelo menos duas pessoas antes do merge. A revisão fica registrada no pull request.

A política é pública e canônica. Não há histórico de versões nem aumento de versão antes da produção. O texto vigente descreve a regra atual.

## Glossário

- **Agente autônomo:** sistema que abre, comenta, revisa, aprova ou mergeia sem uma pessoa decidir no momento da ação.
- **Anotador automático (notetaker):** ferramenta que transcreve ou resume reunião. Só entra com consentimento.
- **Declaração de uso de IA (disclosure):** informação sobre ferramenta, partes assistidas e revisão humana.
- **Falso negativo:** modelo deixa de sinalizar ou classificar um caso que deveria ser sinalizado.
- **Falso positivo:** modelo sinaliza ou classifica um caso que não deveria ser sinalizado.
- **Inferência:** execução de um modelo para produzir transcrição, descrição, tradução, resumo, classificação ou pontuação.
- **Lavagem de licença (license laundering):** usar IA para reescrever ou disfarçar obra de terceiros e escapar de licença, atribuição ou permissão.
- **Modelo:** componente treinado que produz a inferência. O projeto registra nome e versão.
- **Output (saída):** resultado produzido pelo modelo, como texto, classificação, transcrição ou resumo.
- **Prompt:** instrução ou conjunto de instruções enviado ao modelo. Tem versão registrada.
- **Proveniência:** registro de origem, modelo, versão, confiança e conteúdo bruto que permitem rastrear o output.
- **Viés:** resultado sistematicamente distorcido contra ou a favor de um grupo, contexto ou tipo de conteúdo.

## Referências

- [Código de conduta](CODE_OF_CONDUCT.md)
- [Segurança da comunidade](COMMUNITY_SAFETY.md)
- [Segurança da informação](SECURITY.md)
- [Governança](GOVERNANCE.md)
- [Guia de contribuição](CONTRIBUTOR_HANDBOOK.md)
- [CLA](CLA.md)
- [Como usar IA no produto](https://docs.redecivica.com.br/modelos-de-inferencia/)
- [Onde a IA atua no livro](https://docs.redecivica.com.br/rede-civica/#onde-a-ia-atua)
