# Governança da Rede Cívica

Este documento descreve como a Rede Cívica decide, quem responde por cada área e como a governança muda. Ele vale para todos os espaços da organização: repositórios, issues, pull requests, discussões, chamadas, eventos e canais de beta.

A governança é pública. Decisões e justificativas ficam registradas em issue, pull request ou ata. Nenhuma decisão que afete o projeto público é tomada em canal privado.

## Estado atual

O projeto está em alpha fechado. O aplicativo opera com dados de teste e convidados. A abertura para uso por terceiros está prevista para 2027.

A organização ainda não constituiu a fundação prevista no livro. Até a constituição, a decisão final é do fundador, com consulta aos owners de continuidade quando nomeados. Depois da fundação, a decisão passa ao conselho da fundação, com mandatos rotativos e as regras deste documento incorporadas ao estatuto.

O código oficial é AGPL-3.0. O texto é CC BY-SA 4.0. A marca segue a política de marca. O CLA permanece como instrumento de contribuição.

## Princípios

1. **Transparência.** Propostas, decisões e justificativas são públicas. As exceções são dados pessoais, segredos, vulnerabilidades em tratamento e casos de conduta.
2. **Consenso preguiçoso.** Silêncio qualificado não bloqueia. Oposição precisa de motivo técnico ou de princípio e de alternativa.
3. **Responsabilidade humana.** Uma pessoa humana responde por toda contribuição e por toda decisão. IA não decide, não prioriza e não publica sem revisão.
4. **Proteção de quem discorda.** Discordar da tese é legítimo. A tese não é teste de lealdade. Assédio não é dissentimento.
5. **Fork como último recurso.** A licença garante que o código e o texto permanecem livres. O fork é a saída se a governança for capturada e os mecanismos internos falharem.

## Papéis

| Papel | Permissão no GitHub | Critério | Responsabilidade |
|---|---|---|---|
| Owner de continuidade | Owner | Confiança do fundador e 2FA | Acesso de emergência, merge e sucessão |
| Owner ativo | Owner | Owner de continuidade com atuação institucional | Decisão institucional e segurança da organização |
| Mantenedor | Write ou Maintain | Três contribuições relevantes e um ciclo de review | Merge, release, triagem, revisão e mentoria |
| Revisor | Triage ou Write | Dois reviews aprovados | Review técnico sem merge |
| Triager (organizador de issues) | Triage | Um mês de triagem | Labels, duplicatas, boas-vindas e encaminhamento |
| Contribuidor | Read | Primeiro pull request aceito | Código, documentação, design, teste, tradução e comunidade |
| Moderador de comunidade | Write em Discussions | Indicação e treinamento | Moderação de espaços, conflito e incidente |

O fundador acumula, até a fundação, as funções de owner ativo, mantenedor ativo e decisão final. A lista nominal está em [MAINTAINERS.md](MAINTAINERS.md). Os critérios de progressão estão em [CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md).

Owner de continuidade não conta como mantenedor ativo sem review ou merge no período. A permissão de owner garante continuidade de acesso. Ela não substitui presença na revisão.

## Como as decisões são tomadas

### Consenso preguiçoso (decisão sem votação)

Consenso preguiçoso é a regra de decisão sem votação. A proposta segue se ninguém apresentar uma objeção fundamentada dentro do prazo. Silêncio conta como concordância.

- Decisão operacional: pull request com descrição do problema e da solução. Prazo de 7 dias para comentários. Um mantenedor decide.
- Decisão substantiva: proposta pública de mudança com prazo de 14 dias. Duas aprovações de mantenedores ou revisores.
- Decisão de princípio: proposta pública de mudança com prazo de 30 dias. Aprovação do fundador e consulta aos owners de continuidade.
- Decisão de segurança: tratamento privado, com divulgação coordenada.
- Decisão de conduta: fluxo próprio, definido no [código de conduta](CODE_OF_CONDUCT.md) e no [plano de segurança da comunidade](COMMUNITY_SAFETY.md).

Uma objeção é válida quando identifica risco concreto, princípio afetado ou custo relevante e propõe alternativa. Preferência pessoal não suspende a decisão. Quem decide registra a objeção e a resposta.

Enquanto houver menos de dois mantenedores ativos, o fundador decide as matérias substantivas e registra a decisão com a justificativa. A consulta aos owners de continuidade e as duas aprovações passam a valer quando as pessoas existirem.

### Proposta pública de mudança (RFC)

Mudança substantiva ou de princípio passa por uma proposta pública de mudança, chamada aqui de RFC. A sigla vem do inglês Request for Comments, pedido de comentários. A proposta é uma issue pública com o título `RFC: <tema>` e as seções:

- Problema.
- Proposta.
- Alternativas consideradas.
- Impacto em código, dados, contratos e documentação.
- Segurança e privacidade.
- Licença e origem de contribuição.
- Uso de IA, quando houver.
- Migração e rollback.
- Questões abertas.

O prazo de comentários é de 14 dias para mudança substantiva e de 30 dias para mudança de princípio. A decisão é registrada em comentário final, com data, resultado, justificativa e posições contrárias. Proposta rejeitada é fechada com o motivo. Ela pode ser reaberta com evidência nova.

Correção de segurança pode entrar antes da proposta, com nota pública em até 5 dias úteis. Mudança de princípio nunca é emergencial.

### Veto

O veto protege os princípios fundadores. Ele não serve para bloqueio silencioso nem para preferência técnica.

- **Quem veta.** Até a fundação, o fundador. Depois da fundação, o conselho, com maioria de 2/3 para matéria de princípio.
- **Escopo.** Qualquer mudança que reduza transparência, dificulte auditabilidade, centralize decisão que era distribuída ou distorça os princípios fundadores.
- **Fora do escopo.** Otimização técnica, expansão de funcionalidade que amplie participação ou transparência e ajuste operacional que não afete princípio.
- **Forma.** Parecer público em até 5 dias úteis, com a decisão, o princípio afetado e o trecho da proposta.
- **Efeito.** Veto sem justificativa pública e sem vínculo ao princípio não suspende a decisão.
- **Contestação.** A comunidade tem 14 dias para apresentar reformulação, evidência contrária ou pedido de revisão. A proposta reformulada pode ser reapresentada.

### Conflito de interesse

Quem participa de uma decisão declara conflito antes de opinar. Conflito inclui interesse comercial, vínculo empregatício, relação familiar, disputa pessoal e participação no caso.

A pessoa em conflito se afasta do review, da decisão e da moderação. O afastamento é registrado sem detalhe pessoal. Se o fundador estiver em conflito, os owners de continuidade decidem por maioria. Se não houver owners nomeados ou todos estiverem em conflito, uma pessoa externa de confiança decide e o parecer é público.

### Apelação

- **Decisão operacional.** Pedido de reconsideração ao mantenedor. Se persistir, o fundador decide.
- **Decisão substantiva.** Revisão da proposta com evidência nova. O fundador decide depois de ouvir os owners de continuidade.
- **Decisão de princípio.** Os owners de continuidade decidem por maioria. Quando não houver owners nomeados, o fundador decide com parecer externo. Depois da fundação, o conselho decide.
- **Conduta.** O fluxo de apelação está no [código de conduta](CODE_OF_CONDUCT.md) e no [plano de segurança da comunidade](COMMUNITY_SAFETY.md).
- **Segurança.** Não há apelação pública. O caso segue a divulgação coordenada.

## Registro público de decisões

Toda decisão substantiva tem uma issue ou um pull request público. O comentário final registra a decisão, a justificativa, a data, os dissentimentos e os links relevantes.

O histórico de issues e pull requests com o título `Governança:` é o registro público de decisões. O resumo mensal é publicado no espaço público da organização. Nenhuma decisão que afete o projeto público fica apenas em conversa privada.

## Licença e compromissos

O código oficial permanece AGPL-3.0. O texto permanece CC BY-SA 4.0. A marca segue a [política de marca](TRADEMARK.md).

Não há relicenciamento unilateral. Mudança de licença exige proposta pública de mudança, 30 dias de comentários, aprovação do fundador e consulta aos owners de continuidade, com justificativa jurídica pública. O CLA permite ao Titular relicenciar. Essa permissão não é usada para contornar este processo.

A fundação ficará com a missão e a marca, não com o código. O código continua AGPL-3.0 e o fork continua possível. A transferência da marca para a fundação exige consulta pública e o mesmo processo de mudança de princípio.

Toda contribuição exige aceite do [CLA](CLA.md). A origem do conteúdo é declarada. Contribuição sem origem clara é recusada.

## Caminho até a fundação

| Etapa | Critério | O que muda |
|---|---|---|
| Organização em formação | Fundador, owners de continuidade, governança publicada e mantenedores ativos | Decisão final do fundador, com consulta aos owners |
| Pré-fundação | Três mantenedores ativos, cinco contribuidores externos com pull request mergeado, dois encontros mensais abertos realizados, seis meses de registro público de decisões, código de conduta testado e primeira medição de contribuição, tempo de resposta e issues paradas publicada | Consulta pública do estatuto |
| Consulta | 30 dias de comentários públicos, revisão de duas pessoas e ata publicada | Estatuto revisado |
| Constituição | CNPJ, estatuto e conselho com mandatos rotativos | Conselho eleito por contribuidores ativos |
| Transição | Transferência da marca e da governança, com o código mantido em AGPL-3.0 | Fundação detém a missão e a marca |

O conselho da fundação tem mandatos rotativos. Nenhum assento é vitalício. Nenhuma decisão estratégica é tomada sem publicação prévia e período de comentários.

O veto de princípio exige maioria de 2/3 e parecer público que vincule o veto ao princípio específico. Todo veto tem 14 dias de contestação. A comunidade pode apresentar reformulação, evidência contrária ou pedido de revisão.

A licença é a última instância. Se a fundação for capturada de forma irreversível e os mecanismos internos falharem, a comunidade pode manter uma versão independente do projeto.

A constituição jurídica depende de recursos e de assessoria jurídica. O compromisso é não antecipar a fundação sem os critérios públicos acima.

## Compromissos

- Publicar toda mudança de governança com antecedência mínima de 14 dias, e 30 dias para mudança de princípio.
- Submeter mudanças de governança à revisão de duas pessoas.
- Manter o registro público de decisões.
- Responder a primeira mensagem em issue ou pull request em até 2 dias úteis.
- Publicar relatório anual de conduta, com número de casos, tempo de resposta e medidas, sem identidade. O formato está em [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).
- Publicar relatório mensal com contribuição, tempo de resposta e issues paradas quando a primeira medição existir.
- Não incluir dado pessoal em métrica, relatório, issue ou discussão.
- Não citar documento interno em arquivo público.
- Manter a divulgação coordenada de segurança.
- Manter o compromisso de licença descrito acima.

## Como mudar este documento

Mudança neste documento exige proposta pública de mudança com 30 dias de comentários, revisão de duas pessoas e aprovação do fundador, com consulta aos owners de continuidade. Depois da fundação, a mudança segue o estatuto e o conselho.

Enquanto não houver uma segunda pessoa revisora, a mudança é publicada com justificativa e fica aberta a comentários por 30 dias antes do merge. A revisão de duas pessoas passa a valer quando a segunda pessoa existir.

Nenhuma mudança entra por commit unilateral.
