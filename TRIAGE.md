# Triagem

A triagem classifica issues e pull requests, responde à primeira mensagem e encaminha o trabalho. Ela vale para todos os repositórios da organização.

O label `needs-triage` indica que o item ainda não passou pela triagem. A remoção do label marca a classificação concluída.

A triagem é pública. Issue, pull request e Discussão são os canais de trabalho. Relato de vulnerabilidade e de conduta não entra em issue. Os canais estão em [SECURITY.md](SECURITY.md) e [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## Papéis

| Papel | Permissão no GitHub | Responsabilidade |
|---|---|---|
| Triager | Triage | Lê itens novos, aplica labels, responde, pede informação, fecha duplicata e encaminha. |
| Mantenedor | Write ou Maintain | Faz triagem, revisão, merge, release e mentoria. Decide escopo e prioridade. |
| Direção | Owner | Decide conflito de prioridade, bloqueio de longo prazo e sucessão. |

Os critérios de progressão estão em [CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md). A lista nominal está em [MAINTAINERS.md](MAINTAINERS.md).

## Rotina semanal

A triagem acontece uma vez por semana, em 30 minutos, na segunda-feira. Feriado desloca a triagem para o próximo dia útil.

Checklist da sessão:

1. Ler issues e pull requests novos.
2. Aplicar label de classificação.
3. Responder à primeira mensagem em até 5 dias úteis.
4. Pedir a informação que falta, com perguntas específicas.
5. Fechar duplicata com link para a issue original.
6. Indicar mentor nas tarefas de primeira contribuição.
7. Revisar itens parados há 30 dias.
8. Atualizar o roadmap quando a prioridade mudar.

A sessão não precisa de ata. A decisão fica registrada no próprio item, em comentário.

## Prazos

| Item | Prazo | Ação |
|---|---|---|
| Primeira resposta humana | 5 dias úteis | Resposta pública em issue, discussão ou pull request. |
| Triagem semanal | Segunda-feira, 30 minutos | Classificação, labels e encaminhamento. |
| Issue parada | 30 dias sem resposta ou atividade | Revisão de triagem, comentário e decisão. |
| Pull request parado | 30 dias sem atividade | Comentário. Se continuar parado por 7 dias, pode ser fechado. |

O prazo conta dias úteis, de segunda a sexta, no fuso de São Paulo. A ausência de prazo de correção, merge ou release está em [SUPPORT.md](SUPPORT.md).

## Labels

A taxonomia é única para os seis repositórios. A tabela usa os mesmos nomes dos formulários e do [guia de contribuição](CONTRIBUTOR_HANDBOOK.md#labels).

| Label | Quando aplicar | Quando remover |
|---|---|---|
| `needs-triage` | Todo item novo, até a primeira classificação. | Depois da classificação. |
| `bug` | Comportamento incorreto reproduzível. | Se não for reproduzível ou for duplicata. |
| `enhancement` | Melhoria ou funcionalidade nova. | Se a proposta for recusada ou virar outra issue. |
| `docs` | Mudança em documentação, guia, referência ou texto. | Quando o item for classificado em outra área. |
| `question` | Dúvida sobre uso, contrato ou modelo. | Quando a dúvida for respondida e o item fechado. |
| `good first issue` | Tarefa que atende aos critérios abaixo. | Quando a tarefa deixar de ser adequada ou for concluída. |
| `help wanted` | Tarefa com escopo definido e sem pessoa responsável. | Quando alguém assumir ou a tarefa for bloqueada. |
| `mentor` | Tarefa de primeira contribuição com mentor indicado. | Quando a tarefa for concluída ou o mentor mudar. |
| `blocked` | Tarefa que depende de outra mudança ou decisão. | Quando a dependência for resolvida. |
| `ai-assisted` | Contribuição com uso de IA declarado. | O uso declarado permanece no histórico. |

A label `accessibility` já existia no `.github` e continua em uso para relatos de barreira de acessibilidade. Ela segue a mesma regra: aplica no relato e sai quando o item for classificado em outra área.

## Critérios de `good first issue`

Uma issue recebe a label quando tem:

- contexto que explica o problema e o resultado esperado;
- critério de aceite verificável;
- arquivos ou área prováveis;
- tempo estimado declarado;
- mentor indicado na label `mentor`;
- escopo independente de decisão de arquitetura, contrato ou governança;
- nenhum dado pessoal, credencial ou conteúdo de terceiros;
- gate do repositório identificado.

Antes de aplicar a label, o triager confere os oito itens e comenta o que falta. A issue sem mentor não recebe `good first issue`. A issue que depende de outra mudança recebe `blocked` e não entra na lista de primeiras tarefas.

A pessoa que quer trabalhar comenta na issue. O triager confirma o interesse e atribui quando possível. A label permanece até a conclusão ou até a issue deixar de ser adequada.

## Critérios de `help wanted`

A label `help wanted` indica que a tarefa precisa de ajuda. Ela é aplicada quando:

- o escopo está definido;
- não há pessoa responsável;
- a tarefa pode ser feita por mais de uma pessoa ou dividida em partes;
- a tarefa não está bloqueada.

A issue descreve o que falta, onde começar e como pedir ajuda. A label pode conviver com `good first issue` quando a tarefa também for adequada para a primeira contribuição.

A label é removida quando alguém assume a tarefa ou quando a tarefa passa a depender de outra mudança.

## Critérios de `blocked`

A label `blocked` indica dependência externa. Ela exige:

- a dependência nomeada, com link para issue, decisão ou release;
- a condição objetiva para desbloquear;
- a pessoa ou o papel que acompanha a dependência.

O triager revisa itens com `blocked` a cada 30 dias. Se a dependência fechar, a label é removida e o item volta para a fila. Se a dependência não tiver prazo, a issue continua aberta e explica o motivo no comentário.

## Fechamento

Nenhum item é fechado sem comentário. O comentário diz o motivo e o próximo passo.

| Situação | Quem fecha | Regra |
|---|---|---|
| Duplicata | Triager | Linkar a issue original e fechar como duplicata. |
| Falta de informação | Triager | Fazer perguntas específicas. Se não houver resposta em 30 dias, fechar com nota. A pessoa pode reabrir. |
| Fora do escopo | Mantenedor | Explicar o motivo e linkar o roadmap ou a governança. |
| Resolvido | Mantenedor | Linkar o pull request ou commit e fechar depois do merge. |

A issue sem informação suficiente não é fechada no mesmo dia. O pedido de complemento fica registrado e a pessoa tem tempo para responder.

A issue sem resposta por 30 dias entra na revisão de triagem. A revisão decide entre pedir informação, aplicar `help wanted`, aplicar `blocked` ou fechar com nota.

## Segurança e conduta

- Vulnerabilidade de segurança não entra em issue. O relato segue [SECURITY.md](SECURITY.md).
- Relato de conduta não entra em issue. O canal e os prazos estão em [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) e [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).
- Issue, pull request, exemplo e formulário não pedem dado pessoal, credencial, token ou conteúdo de terceiros.
- Se um item contiver dado pessoal ou segredo, a triagem remove o conteúdo, avisa a pessoa por canal privado e registra o incidente. Segredo exposto exige rotação imediata.
- A triagem não pede endereço, documento, localização precisa, áudio ou imagem de terceiros para reproduzir um problema. Use dado de teste.

## IA

O uso de IA é declarado em issue, discussão e pull request, conforme [AI_POLICY.md](AI_POLICY.md). A label `ai-assisted` marca a contribuição que declarou o uso.

A triagem confere a declaração antes da revisão. Se faltar, pede a ferramenta, as partes assistidas e o que foi revisado por uma pessoa. A declaração não garante aceitação.

Agente autônomo não abre, revisa, aprova nem mergeia pull request. Pull request nesse formato é fechado com link para a política. A pessoa responsável pode reenviar o trabalho com autoria humana e declaração.

Erro, viés ou falso positivo de modelo vai para a categoria Feedback de modelo nas [Discussões](https://github.com/Rede-Civica/.github/discussions). Não use issue para dado de teste com informação pessoal.

Pull request em massa sem issue prévia é fechado com pedido de issue. A regra vale para contribuição humana e assistida.

## Onde pedir ajuda

| Assunto | Canal |
|---|---|
| Dúvida de triagem, label ou encaminhamento | [Discussões, categoria Ajuda](https://github.com/Rede-Civica/.github/discussions/categories/ajuda) |
| Suporte e prazos | [SUPPORT.md](SUPPORT.md) |
| Progressão para triager ou mantenedor | [CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md) |
| Governança | [GOVERNANCE.md](GOVERNANCE.md) |
