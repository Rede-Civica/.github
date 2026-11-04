# Suporte

Este documento diz onde perguntar, onde reportar cada tipo de problema e o que esperar. O projeto está em alpha fechado. Não há SLA de produção.

## Canais

| Assunto | Canal | O que incluir |
|---|---|---|
| Dúvida de uso, instalação, contribuição ou documentação | [Discussões](https://github.com/Rede-Civica/.github/discussions), categoria Ajuda | Versão, sistema, passo a passo e erro completo |
| Contribuição, primeiro PR e gates | [Guia de contribuição](CONTRIBUTOR_HANDBOOK.md) | Setup, fluxo, labels, CLA e revisão |
| Conversa, ideia ou projeto da comunidade | [Discussões](https://github.com/Rede-Civica/.github/discussions) | Categoria, contexto e o que já tentou |
| Erro, viés ou falso positivo de modelo | [Discussões](https://github.com/Rede-Civica/.github/discussions), categoria Feedback de modelo | Tarefa, modelo e versão, resultado esperado, resultado observado e dados de teste |
| Revisão de decisão de moderação de conteúdo | contato@redecivica.com.br, assunto `Moderação de conteúdo` | Link do conteúdo, decisão e motivo da contestação. Não inclua dado pessoal |
| Encontros mensais abertos | [ENCONTROS.md](ENCONTROS.md) | Pauta, condições e como participar |
| Bug reproduzível | Issue com o template de bug | Passos, resultado esperado, resultado atual e ambiente |
| Proposta de funcionalidade | Issue com o template de funcionalidade | Problema, proposta, alternativas e impacto |
| Vulnerabilidade | [SECURITY.md](SECURITY.md) | Detalhes em canal privado, sem issue pública |
| Conduta | [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) e [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md) | Relato confidencial, prazos, medidas provisórias e apelação |
| Governança | Issue com o título `Governança: <tema>` | Proposta, princípio afetado e alternativa |
| Imprensa, parceria ou assunto institucional | contato@redecivica.com.br | Contexto e prazo |

As issues da organização ficam em [github.com/Rede-Civica/.github/issues](https://github.com/Rede-Civica/.github/issues). Use o template mais próximo do assunto.

As [Discussões](https://github.com/Rede-Civica/.github/discussions) estão abertas e são o espaço público para dúvidas, ideias e conversa. As regras e as categorias estão em [DISCUSSIONS.md](DISCUSSIONS.md). Issues ficam para bug reproduzível, proposta com escopo e trabalho que precisa de registro.

A [política de IA](AI_POLICY.md) explica como o projeto usa IA, como declarar o uso e como funciona a contestação. Erro de modelo tem canal na categoria Feedback de modelo. Não publique dado pessoal, mídia de terceiros ou credencial.

## Prazos

- Primeira resposta humana em issue, discussão ou pull request: até 2 dias úteis.
- Relato de segurança: confirmação em até 5 dias úteis. O fluxo completo está em [SECURITY.md](SECURITY.md).
- Relato de conduta: confirmação em até 3 dias úteis e decisão inicial em até 10 dias úteis. O fluxo completo está em [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).
- Feedback de modelo: primeira resposta humana em até 2 dias úteis. A triagem pode abrir uma issue ou uma correção, sem prazo garantido.
- Revisão de pull request: primeira resposta em até 2 dias úteis. Se a revisão precisar de mais tempo, o mantenedor diz quando volta.
- Não há prazo garantido para correção, merge ou release.

O prazo conta dias úteis, de segunda a sexta, no fuso de São Paulo. Feriados locais podem atrasar a resposta.

## Triagem semanal

A triagem acontece uma vez por semana, em 30 minutos, na segunda-feira. Feriados podem deslocar a triagem para o próximo dia útil.

Na triagem, os mantenedores leem issues e pull requests novos, aplicam labels, respondem a primeira mensagem, pedem informação que falta, fecham duplicata com link para a original, indicam mentor nas tarefas de primeira contribuição e atualizam o roadmap quando a prioridade muda.

O label `needs-triage` indica que a issue ainda não foi classificada. O label `mentor` indica que a tarefa tem uma pessoa mentora.

## Pull request parado

O pull request parado há 30 dias sem atividade recebe um comentário. Se continuar parado por 7 dias, pode ser fechado com uma nota. A pessoa pode reabrir quando retomar o trabalho.

O label `blocked` indica que o pull request depende de outra mudança ou de uma decisão. O bloqueio é explicado em comentário.

## Versões suportadas

| Versão | Suporte |
|---|---|
| `main` | Sim, é a referência atual |
| `develop` | Correções direcionadas |
| Releases públicas | Nenhuma release pública até esta publicação |

O projeto não publica releases versionadas antes da produção. `main` é a referência. Interfaces, contratos e dados de teste podem mudar sem aviso durante o alpha e o beta.

## Escopo

O suporte cobre:

- Instalação e execução local.
- Tutoriais, guias, referências e documentação.
- Fluxo de contribuição, CLA, gates e revisão.
- Bug reproduzível e proposta de funcionalidade.
- Erro, viés ou falso positivo de modelo, pelo canal de feedback.
- Acessibilidade e experiência em navegador ou celular.
- Vulnerabilidade de segurança, pelo canal privado.

O suporte não cobre:

- Disponibilidade de produção, prazo de correção ou contrato de nível de serviço.
- Consultoria privada, desenvolvimento sob encomenda ou suporte pago.
- Infraestrutura de terceiros, provedor de nuvem ou rede local.
- Orientação jurídica, contábil ou de políticas públicas.
- Atendimento de emergência, denúncia de crime ou pedido que dependa de órgão público.
- Dados pessoais reais. Use dados de teste.

O aplicativo não é canal oficial do poder público. Ele não garante resposta de prefeitura, secretaria ou empresa.

## Como ajudar em 30 minutos

Não é preciso escrever código para contribuir. Estas tarefas cabem em meia hora:

| Tarefa | Tempo | Onde começar |
|---|---|---|
| Ler o começo do livro e apontar um trecho confuso | 15 min | Abra uma issue com a página e o trecho |
| Rodar o tutorial local e relatar o passo que falhou | 30 min | Siga o [tutorial de execução local](https://docs.redecivica.com.br/tutoriais/rodando-o-projeto-localmente/) e abra uma issue |
| Revisar uma página e apontar link quebrado ou erro de texto | 10 min | Abra uma issue com o endereço da página |
| Reproduzir um bug aberto e acrescentar seu ambiente | 20 min | Comente na issue com sistema, navegador e passos |
| Responder a dúvida de outra pessoa | 15 min | Responda na discussão ou issue com o que funcionou para você |
| Testar o aplicativo no celular e relatar layout ou acessibilidade | 20 min | Abra uma issue com captura sem dado pessoal |
| Apresentar o projeto a uma pessoa que trabalha com tecnologia cívica | 5 min | Envie o site [docs.redecivica.com.br](https://docs.redecivica.com.br) |

Toda contribuição segue o [CLA](CLA.md) e o código de conduta. A issue é o lugar para alinhar o trabalho antes do pull request. O [guia de contribuição](CONTRIBUTOR_HANDBOOK.md) mostra o setup, o primeiro PR e os gates.

## Segurança e privacidade

- Não publique dado pessoal, credencial, token ou conteúdo de terceiros em issue, discussão ou pull request.
- Não registre demanda real, endereço de pessoa, foto de documento ou dado sensível no ambiente de teste.
- Relato de vulnerabilidade segue [SECURITY.md](SECURITY.md). Não abra issue pública com detalhe de exploração.
- Pedido de titular de dados segue a [política de privacidade](https://docs.redecivica.com.br/politica-privacidade/) publicada no site.

## Conduta

A convivência segue o [código de conduta](CODE_OF_CONDUCT.md). Discordar da tese é legítimo. Assediar não é. A tese não é teste de lealdade para contribuir.

O canal atual de relato é contato@redecivica.com.br. O relato é confidencial e tratado pelos respondedores indicados no [código de conduta](CODE_OF_CONDUCT.md). O fluxo completo, com triagem, medidas provisórias, prazos e apelação, está em [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).

## Como o suporte é mantido

Os mantenedores fazem triagem semanal. Issue sem informação suficiente pode ser fechada com um pedido de complemento. A pessoa pode reabrir quando tiver os dados que faltam.

A issue não é o lugar de conversa privada. Assunto sensível vai por e-mail.
