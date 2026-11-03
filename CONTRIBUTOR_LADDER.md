# Escada de contribuição

A escada descreve como uma pessoa passa de contribuidora a mantenedora e como a direção da organização é exercida. Os critérios são públicos, cumulativos e verificáveis no histórico do GitHub.

Contribuição vale em código, documentação, design, testes, tradução, triagem, revisão e comunidade. Nenhum tipo é inferior. O que conta é o efeito no projeto e a qualidade da evidência.

## Princípios

- A pessoa começa pelo primeiro pull request aceito. Não há período de espera.
- A progressão é por convite ou candidatura, com evidência pública.
- Discordar não bloqueia a progressão. O código de conduta é o limite.
- A pessoa pode pausar quando quiser, sem penalização.
- A permissão no GitHub acompanha o nível. O nível não é um título honorário.
- A decisão considera o conjunto da contribuição, não o volume de commits.

## Níveis

| Nível | Permissão no GitHub | Critérios | Tempo mínimo | Evidência | Responsabilidade |
|---|---|---|---|---|---|
| Contribuidor | Read | Primeiro pull request aceito | Nenhum | Pull request mergeado | Seguir o código de conduta, o CLA e os gates do repositório |
| Triager (organizador de issues) | Triage | Dez issues triadas com label, resposta e encaminhamento | Um mês de atividade | Links das issues e das decisões | Labels, duplicatas, boas-vindas e encaminhamento |
| Revisor | Triage ou Write | Dois reviews aprovados em pull requests diferentes | Um mês como contribuidor | Links dos reviews | Review técnico sem merge |
| Mantenedor | Write ou Maintain | Três contribuições relevantes, um ciclo completo de review e dois avais de mantenedores | Três meses de atividade | Pull requests, reviews e participação em [propostas públicas de mudança](GOVERNANCE.md#proposta-pública-de-mudança-rfc) | Merge, release, triagem, review e mentoria |
| Direção | Owner | Confiança do fundador e 2FA para continuidade. Owner ativo exige atuação institucional | Seis meses como mantenedor para owner ativo | Registro público da nomeação e histórico de decisões | Decisão institucional, segurança da organização e sucessão |
| Moderador de comunidade | Write em Discussions | Um mês de participação, treinamento e uma indicação | Um mês | Histórico de participação e treinamento | Moderação, conflito e incidente, com recusa por conflito de interesse |

Contribuição relevante é a mudança mergeada que resolve um problema real e inclui teste, documentação ou evidência equivalente. Correção de typo e link quebrado conta para o primeiro pull request. Ela não sustenta sozinha a progressão para mantenedor.

O nível de direção não é recompensa por volume. Ele exige julgamento, disponibilidade e confiança. Até a fundação, o fundador nomeia os owners de continuidade. Depois da fundação, o conselho é eleito pelos contribuidores ativos, conforme o estatuto.

## Trilha de comunidade

A moderação é uma função paralela. O moderador não precisa ser mantenedor. Ele precisa conhecer o [código de conduta](CODE_OF_CONDUCT.md), o [plano de segurança da comunidade](COMMUNITY_SAFETY.md), as regras das [Discussões](DISCUSSIONS.md) e os limites da categoria política.

O moderador é indicado, participa de treinamento e atua com recusa por conflito de interesse. A função não dá poder de decisão sobre código ou rumo do projeto.

## Como pedir progressão

1. Abra uma issue com o título `Escada: <nome>` ou fale com um mantenedor.
2. Liste a evidência: pull requests, reviews, issues triadas, documentação e outras contribuições.
3. Um mantenedor confirma os critérios em até 7 dias. Se faltar algo, diz o que falta e o próximo passo.
4. A decisão é por consenso preguiçoso dos mantenedores, com 7 dias para objeção. O fundador decide em caso de empate.
5. Aprovada a progressão, o mesmo pull request atualiza [MAINTAINERS.md](MAINTAINERS.md), a permissão no GitHub e o registro público.
6. Reprovada a progressão, a pessoa recebe o motivo e pode reapresentar depois de 30 dias.

A candidatura pode ser feita pela própria pessoa. A indicação por um mantenedor é bem-vinda e não é obrigatória.

## Pausa, inatividade e saída

- **Pausa.** A pessoa avisa um mantenedor. Não há penalização. A permissão é mantida por 90 dias.
- **Inatividade.** Depois de 90 dias sem contribuição, review ou triagem, a pessoa entra em pausa em [MAINTAINERS.md](MAINTAINERS.md). Depois de 180 dias, passa a emérita e a permissão de escrita é reduzida para Read.
- **Retorno.** Uma contribuição e a aprovação de um mantenedor restauram o nível anterior.
- **Saída por conduta.** Segue o [código de conduta](CODE_OF_CONDUCT.md) e o [plano de segurança da comunidade](COMMUNITY_SAFETY.md), com medidas proporcionais e direito de apelação.
- **Owner de continuidade.** A saída é decidida pelo fundador com os demais owners, com 2FA e registro público. A sucessão é definida antes da saída.
- **Discordância.** Discordar da tese, do roadmap ou de uma decisão não é motivo de remoção.

## Reconhecimento

O reconhecimento usa o histórico público, as notas de marco e a lista de contribuidores. A pessoa é incluída com consentimento. A saída por inatividade não apaga o histórico.

## Ligação com as permissões

| Nível | Permissão |
|---|---|
| Contribuidor | Read |
| Triager (organizador de issues) | Triage |
| Revisor | Triage ou Write |
| Mantenedor | Write ou Maintain |
| Direção | Owner |
| Moderador de comunidade | Write em Discussions |

A permissão é concedida no mesmo dia da atualização da lista. A permissão não é retirada sem registro público, salvo medida provisória de segurança ou conduta, que é registrada depois do caso.
