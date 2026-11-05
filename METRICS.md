# Métricas de saúde da comunidade

Este documento publica a primeira medição da saúde da comunidade da Rede Cívica, as definições usadas, as metas para fevereiro de 2027 e a cadência do relatório mensal.

A medição segue três modelos do CHAOSS (Community Health Analytics Open Source Software): saúde de projeto inicial (Starter Project Health), acolhimento da comunidade (Community Welcomingness) e viabilidade de projeto de software aberto (OSS Project Viability Starter). A primeira medição foi feita em 04/11/2026. Os modelos de segurança (Safety) e governança de IA (AI Governance) entram antes do lançamento público.

O relatório mede tendência, contexto e decisão. Não compara projetos e não rankeia pessoas. Nenhum dado pessoal é publicado.

## Como ler a tabela

- **Janela:** 90 dias encerrados na data da medição.
- **Contribuidor:** pessoa que assinou um commit ou teve contribuição mergeada no período. Bots não contam.
- **Organização:** domínio de e-mail corporativo do commit. Provedores públicos e endereços `noreply` contam como pessoa independente.
- **Mediana:** valor que separa a metade maior da metade menor de uma lista.
- **n/a:** não há dado suficiente para calcular. O relatório mensal explica o motivo.

## Primeira medição

| Métrica | Definição | Primeira medição (04/11/2026) | Meta fev/2027 | Fonte |
|---|---|---|---|---|
| Fator de ausência de contribuidor (contributor absence factor) | Menor número de pessoas que respondem por 50% dos commits na janela. | 1 | 3 ou mais | Histórico git dos seis repositórios. |
| Fator elefante (elephant factor) | Menor número de organizações que respondem por 50% dos commits na janela. | 1 | 2 ou mais | Histórico git dos seis repositórios. |
| Mantenedores ativos | Pessoas com permissão de merge que revisaram, mergearam ou fizeram commit direto na janela. | 1 | 3 ou mais | Histórico git e dados públicos de pull request. |
| Contribuidores externos | Pessoas fora da organização com pull request mergeado na janela. | 0 | 5 ou mais | API pública e histórico git. |
| Contribuidores não-código | Pessoas fora da organização com contribuição de documentação, design, tradução ou comunidade mergeada na janela. | 0 | 3 ou mais | Histórico de pull requests e registro de contribuições. |
| Tempo até a primeira resposta (time to first response, TTFR) | Mediana de horas entre a abertura e a primeira resposta humana em issue ou pull request. | n/a | 5 dias úteis ou menos | 10 issues públicas abertas em 04/11/2026, sem resposta até a medição. |
| Razão de fechamento de pull request (PR closing ratio) | Pull requests fechados ou mergeados divididos por pull requests abertos na janela. | n/a | 1 ou mais | Nenhum pull request no repositório público. Dados de repositórios privados não entram na medição pública. |
| Idade mediana de issue | Mediana de dias em aberto das issues abertas na data da medição. | 0,2 dia | Menos de 30 dias | 30 issues criadas em 04/11/2026, conforme registro de criação. |
| Marcos públicos | Marcos de desenvolvimento publicados por trimestre. | 0 | 3 | API pública de milestones e registro de marcos. |
| Retenção de novo contribuidor | Percentual de primeiros contribuidores que voltam em 90 dias. | n/a | 40% ou mais | Sem primeiro contribuidor externo na janela. |
| Cobertura de testes | Percentual de linhas cobertas na API e no web. | 92,11% na API e cerca de 94% no web | Manter | Relatório de cobertura de 31/10/2026. |
| OpenSSF Best Practices | Nível do selo do projeto no OpenSSF Best Practices Badge. | Nenhum | Passing | Registro do programa. |
| Casos de conduta | Casos recebidos, tempo de resposta e casos resolvidos. | 0 recebidos, 0 resolvidos, tempo n/a | Acompanhar | Registro do canal de conduta. |

A primeira medição confirma o estado atual: uma pessoa ativa, uma organização e nenhum contribuidor externo. As metas de fevereiro de 2027 medem a mudança desse estado, não a atividade de uma pessoa.

## Metodologia

### Janela e data

A janela cobre os 90 dias encerrados na data da medição. A primeira medição usou o período de 06/08/2026 a 04/11/2026. O relatório mensal usa a janela de 90 dias encerrada na primeira segunda-feira do mês.

### Bots

Contas automatizadas são excluídas de todas as contagens. A exclusão vale para commits, issues, pull requests, comentários, revisões e marcos. Bots conhecidos incluem `dependabot`, `renovate` e `github-actions`.

### Contribuidor e organização

Contribuidor é a pessoa que assinou um commit ou teve contribuição mergeada no período. A contagem por pessoa usa o login do GitHub quando existe e o e-mail do commit quando não existe.

Organização é o domínio de e-mail corporativo do commit. Provedores públicos, como Gmail, Outlook e Yahoo, e endereços `noreply` contam como pessoa independente. A definição evita atribuir uma pessoa a uma empresa que ela não declarou.

### Tempo até a primeira resposta

O tempo até a primeira resposta é a mediana de horas entre a abertura e a primeira resposta humana. A resposta pode ser um comentário ou uma revisão. O autor do item e bots não contam. Itens sem resposta entram no relatório como pendência, não como zero.

### Razão de fechamento de pull request

A razão divide os pull requests fechados ou mergeados na janela pelos pull requests abertos na janela. Um pull request mergeado conta como fechado. Quando não há pull request aberto na janela, a razão fica n/a.

### Idade mediana de issue

A idade mediana usa as issues abertas na data da medição. A idade é a diferença em dias entre a abertura e a data da medição. Issues recém-abertas puxam a mediana para baixo. O número deve ser lido junto com o volume e com o tempo até a primeira resposta.

### Marcos públicos

Marco público é um marco de desenvolvimento publicado no GitHub. A contagem por trimestre mede a cadência pública, não o número de funcionalidades. A primeira medição não registrou marco.

### Cobertura, OpenSSF e conduta

A cobertura de testes vem do relatório de cobertura do período. O OpenSSF Best Practices vem do registro do programa. Os casos de conduta vêm do registro do canal, sem identidade e sem detalhe do caso.

## Limitações da primeira medição

Os repositórios de código estão privados até o lançamento de fevereiro de 2027. A primeira medição usa o histórico git dos seis repositórios e os dados públicos do repositório `.github`. Issues, pull requests e marcos dos repositórios privados entram apenas como agregado operacional. Tempo até a primeira resposta e razão de fechamento de pull request ficam sem dado.

O relatório mensal registra a limitação e a data em que ela deixa de existir. A abertura dos repositórios em fevereiro de 2027 permite medir os dois indicadores com dados públicos.

## Cadência mensal

A medição roda na primeira segunda-feira de cada mês. A primeira edição mensal será em 07/12/2026. O relatório é publicado na categoria Anúncios das Discussões e linkado neste documento.

Cada relatório traz:

- a tabela do mês, com a variação em relação à medição anterior;
- o contexto de mudanças de processo, lançamento ou composição da comunidade;
- uma decisão prática para o mês seguinte;
- as limitações da medição.

O relatório não usa estrelas, seguidores ou número de forks como métrica principal. Esses números medem alcance, não saúde da comunidade.

## Como contestar

Número errado, definição ambígua ou dado faltando: abra uma issue com a label `docs` ou use a categoria Ajuda nas Discussões. Não envie dado pessoal, credencial ou mídia de terceiros.

- [Issues da organização](https://github.com/Rede-Civica/.github/issues)
- [Discussões](https://github.com/Rede-Civica/.github/discussions)
- [Hub da comunidade](https://docs.redecivica.com.br/comunidade/)

## Glossário

- **CHAOSS:** projeto de métricas de saúde para comunidades de software aberto.
- **Fator de ausência de contribuidor (bus factor):** menor número de pessoas que respondem por metade dos commits.
- **Fator elefante:** menor número de organizações que respondem por metade dos commits.
- **Marco público:** marco de desenvolvimento publicado no GitHub.
- **OpenSSF Best Practices:** programa de selo de boas práticas de segurança para projetos de software aberto. O nível Passing é o primeiro nível.
- **Primeira medição (baseline):** retrato inicial usado para comparar a evolução.
- **Pull request:** proposta de mudança que passa por revisão antes do merge.
- **TTFR:** tempo até a primeira resposta humana em issue ou pull request.
