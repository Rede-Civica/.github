# Discussões

As Discussões (GitHub Discussions) são o espaço público de conversa da Rede Cívica. Servem para dúvidas, ideias, projetos da comunidade, conversa sobre governança e debate da tese. Não substituem issues, pull requests, o canal de conduta nem o canal de segurança.

O espaço abre antes do lançamento público. O [código de conduta](CODE_OF_CONDUCT.md) vale em todos os tópicos. A moderação segue este documento e o [plano de segurança da comunidade](COMMUNITY_SAFETY.md).

## Para que servem

| Uso | Categoria |
|---|---|
| Dúvida de uso, instalação, contribuição ou documentação | Ajuda |
| Ideia, melhoria ou experimento | Ideias |
| Projeto da comunidade que usa, estuda ou dialoga com a Rede Cívica | Mostre seu projeto |
| Conversa preliminar sobre governança | Governança |
| Debate da tese, dos princípios e dos valores | Política e valores |
| Relato do grupo de teste | Beta |
| Comunicado oficial e marco do projeto | Anúncios |

## Para que não servem

- Bug reproduzível com passos e ambiente. Use o template de bug nas issues.
- Vulnerabilidade de segurança. Use o canal privado de [SECURITY.md](SECURITY.md).
- Relato de conduta. Use o canal privado de [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
- Proposta pública de mudança (RFC). Abra uma issue com o título `RFC: <tema>`, conforme [GOVERNANCE.md](GOVERNANCE.md).
- Pedido de suporte urgente. Não há plantão 24 horas.
- Divulgação de produto, curso, vaga ou serviço sem relação com o projeto. A moderação pode remover.

## Categorias

| Categoria | Identificador | Formato | O que publicar | Formulário |
|---|---|---|---|---|
| Anúncios | `anúncios` | Comunicado | Comunicados oficiais, marcos e notas. Só mantenedores e moderadores abrem. | Sem formulário |
| Ajuda | `ajuda` | Pergunta e resposta | Dúvidas com contexto e passos. A resposta que resolve é marcada. | `ajuda.yml` |
| Ideias | `ideias` | Discussão aberta | Uma ideia por tópico, com problema, proposta e impacto. | `ideias.yml` |
| Mostre seu projeto | `mostre-seu-projeto` | Discussão aberta | Projetos da comunidade, com link, descrição e relação com a Rede Cívica. | `mostre-seu-projeto.yml` |
| Governança | `governança` | Discussão aberta | Conversa preliminar sobre papéis, decisões e organização. | `governança.yml` |
| Política e valores | `política-e-valores` | Discussão aberta | Debate da tese, dos princípios e dos limites do projeto. | `política-e-valores.yml` |
| Beta | `beta` | Discussão aberta | Relato de jornada do grupo de teste, com dados de teste. | `beta.yml` |

O identificador é o nome que o GitHub usa no endereço da categoria. O GitHub preserva acentos no identificador. Por isso, Anúncios, Governança e Política e valores aparecem com acento na URL. O arquivo do formulário precisa ter o mesmo identificador, inclusive o acento. Se o GitHub gerar um identificador diferente ao criar a categoria, renomeie o arquivo em `.github/DISCUSSION_TEMPLATE/`.

Os formatos aparecem em inglês na interface do GitHub: Announcement (comunicado), Question and answer (pergunta e resposta) e Open-ended discussion (discussão aberta).

## Como abrir uma discussão

1. Procure antes. Use a busca e leia os tópicos fixados.
2. Escolha a categoria mais próxima. A moderação pode mover o tópico.
3. Use o formulário, quando a categoria tiver um.
4. Traga contexto: o que tentou, o que esperava e o que aconteceu.
5. Uma pergunta por tópico. Evite juntar assuntos diferentes.
6. Marque a resposta que resolveu, na categoria Ajuda.
7. Não publique dado pessoal, credencial, token ou conteúdo de terceiros.

## Regras de convivência

1. **Boa-fé.** Presuma boa-fé até haver evidência do contrário. Aponte o problema, não a pessoa.
2. **Contexto.** Diga o que observou, o que inferiu e o que ainda não sabe.
3. **Foco.** Mantenha o tópico na categoria e no assunto. Desvio repetido pode ser movido ou bloqueado.
4. **Privacidade.** Não publique dado pessoal, mensagem privada, captura de tela ou gravação sem consentimento.
5. **Sem spam.** Não repita a mesma mensagem, não abra tópicos iguais e não marque pessoas sem necessidade.
6. **Sem assédio.** Persistência depois de um pedido de parada é assédio. Ameaça, discriminação, doxxing (exposição de dados pessoais) e ataque coordenado são violação.
7. **Sem PR em massa.** Não abra vários pull requests sem issue prévia e sem alinhamento.
8. **Declare IA.** Texto, código ou imagem produzidos com IA seguem a política de IA do projeto, quando publicada. A pessoa que assina o CLA responde pelo conteúdo.
9. **Respeite a moderação.** Medida de moderação se cumpre enquanto estiver vigente. A discordância segue a apelação, não a retaliação.
10. **A tese não é teste de lealdade.** Discordar da tese é legítimo. Ninguém precisa concordar com ela para participar de boa-fé.

## Política e valores

A categoria Política e valores existe para discutir a tese, os princípios e os limites do projeto. Ela tem regra própria porque o projeto tem uma tese política explícita.

- Criticar a tese, apontar risco, defender outra proposta e recusar endosso são legítimos.
- A categoria não é espaço de propaganda eleitoral, campanha partidária ou mobilização para atacar pessoas e instituições.
- Não publique filiação partidária, voto, orientação sexual, religião ou dado pessoal de terceiros.
- Não use a categoria para assediar quem discorda ou para desviar assunto técnico de outra categoria.
- Assunto político que sequestra uma issue técnica pode ser movido para esta categoria, com registro.
- A moderação pode bloquear um tópico com nota pública quando a conversa virar ataque coordenado, ameaça ou exposição de dados.

Discordar da tese não bloqueia contribuição, revisão, progressão ou participação em encontro. O limite é o [código de conduta](CODE_OF_CONDUCT.md).

## Moderação

A moderação começa com o fundador como moderador interino. A segunda vaga está aberta. A lista nominal e a disponibilidade estão em [MAINTAINERS.md](MAINTAINERS.md).

| Ação | Quando |
|---|---|
| Boas-vindas e orientação | Primeira participação ou tópico fora de formato |
| Renomear ou mover | Título confuso ou categoria errada |
| Marcar resposta | Dúvida resolvida na categoria Ajuda |
| Bloquear tópico | Conversa desviada, repetida ou com risco de escalada |
| Ocultar ou remover conteúdo | Violação do código, dado pessoal exposto ou spam |
| Restringir participação | Abuso repetido, com registro e apelação |
| Encaminhar ao respondedor | Ameaça, assédio, doxxing, discriminação ou conteúdo ilegal |
| Encaminhar à segurança | Vulnerabilidade, invasão de conta ou vazamento de dados |

A moderação não decide caso de conduta. Ela contém o dano imediato, preserva a evidência e encaminha o relato ao respondedor. O fluxo completo está em [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).

### Prazos

| Etapa | Prazo |
|---|---|
| Primeira resposta humana | Até 2 dias úteis |
| Risco imediato, ameaça ou doxxing | Mesmo dia |
| Revisão de medida provisória | Até 5 dias úteis |
| Apelação de moderação | Até 10 dias úteis |
| Resposta da apelação | Até 10 dias úteis |

### Conflito de interesse

Quem modera declara conflito antes de agir. Conflito inclui participação no tópico, relação pessoal, vínculo profissional, interesse comercial e disputa anterior. A pessoa em conflito não modera o tópico. Se o fundador estiver em conflito, um advisor externo (pessoa conselheira externa) decide.

### Apelação

A apelação é pedida por escrito ao moderador que não participou da decisão, ou a um advisor externo quando não houver outro moderador livre. A apelação não suspende a medida, salvo decisão em contrário. A decisão é final dentro do projeto. Depois da fundação, o conselho da fundação é a última instância interna.

### Registro e transparência

Cada ação de moderação é registrada com data, tópico, ação e motivo, sem dado pessoal. O registro fica restrito à moderação. O projeto publica um resumo anual com o número de ações por tipo e o tempo de resposta, sem identidade e sem detalhe de caso.

## Conteúdo sensível

- **Ameaça.** Não responda em público. Preserve a captura, o link e o horário. Acione a moderação e o canal de conduta. Em risco imediato, procure o serviço de emergência.
- **Doxxing.** Não repita o dado exposto. Preserve a evidência sem publicar o dado. Acione a moderação para remoção e o canal de conduta.
- **Assédio coordenado.** Não amplifique. Preserve a evidência. A moderação pode bloquear o tópico e restringir contas.
- **Conteúdo ilegal.** Não baixe, copie ou encaminhe. Acione a moderação e a autoridade competente.
- **Vulnerabilidade.** Não publique detalhe de exploração. Use [SECURITY.md](SECURITY.md).

## Post de boas-vindas

Título: `Boas-vindas à Rede Cívica`

Copie o texto abaixo sem os marcadores `>` e publique em Anúncios. Fixe o tópico.

Corpo:

> A Rede Cívica é uma infraestrutura cívica digital para registrar demandas do território, priorizar por parâmetros públicos e acompanhar a execução com rastreabilidade. O projeto está em alpha fechado. O beta aberto está previsto para 2027.
>
> Este é o espaço público de conversa. Aqui você pode tirar dúvidas, propor ideias, mostrar seu projeto, discutir governança e debater a tese. O código de conduta vale em todos os tópicos. Discordar da tese é legítimo. Assediar não é.
>
> **Comece por aqui**
>
> - Entenda o modelo: [livro Rede Cívica](https://docs.redecivica.com.br/rede-civica/).
> - Rode o projeto: [tutorial de execução local](https://docs.redecivica.com.br/tutoriais/rodando-o-projeto-localmente/).
> - Veja quem decide e como: [governança](https://github.com/Rede-Civica/.github/blob/main/GOVERNANCE.md) e [mantenedores](https://github.com/Rede-Civica/.github/blob/main/MAINTAINERS.md).
> - Veja como subir na escada: [escada de contribuição](https://github.com/Rede-Civica/.github/blob/main/CONTRIBUTOR_LADDER.md).
> - Veja o que vem: [roadmap](https://github.com/Rede-Civica/.github/blob/main/ROADMAP.md).
> - Saiba como pedir ajuda e os prazos: [suporte](https://github.com/Rede-Civica/.github/blob/main/SUPPORT.md).
> - Conheça as regras de convivência: [código de conduta](https://github.com/Rede-Civica/.github/blob/main/CODE_OF_CONDUCT.md) e [segurança da comunidade](https://github.com/Rede-Civica/.github/blob/main/COMMUNITY_SAFETY.md).
> - Contribua em 30 minutos: [como ajudar](https://github.com/Rede-Civica/.github/blob/main/SUPPORT.md#como-ajudar-em-30-minutos).
>
> **Ainda em preparação**
>
> A política de IA e a lista de primeiras tarefas (`good first issue`, boa primeira tarefa) serão publicadas antes do lançamento público. Enquanto isso, use a categoria Ajuda para dúvidas e a categoria Ideias para propostas.
>
> **Como usar**
>
> - Escolha a categoria mais próxima.
> - Traga contexto: o que tentou, o que esperava e o que aconteceu.
> - Não publique dado pessoal, credencial ou conteúdo de terceiros.
> - Uma pergunta por tópico. Marque a resposta que resolveu, quando houver.
> - A categoria Beta fica reservada ao grupo de teste. O beta ainda não está aberto.
>
> **Encontros e diário**
>
> Os encontros mensais abertos e o diário público de avanços estão descritos em [ENCONTROS.md](https://github.com/Rede-Civica/.github/blob/main/ENCONTROS.md) e [DEVLOG.md](https://github.com/Rede-Civica/.github/blob/main/DEVLOG.md). A primeira edição dos encontros será marcada depois do lançamento público, quando houver demanda. Não há data marcada.
>
> **Moderação**
>
> A moderação começa com o fundador. A segunda vaga está aberta. A primeira resposta humana sai em até 2 dias úteis. Relatos de conduta não são feitos aqui: use contato@redecivica.com.br.

## Glossário

- **Discussões (GitHub Discussions):** espaço de conversa pública do repositório, separado das issues.
- **Categoria:** agrupamento de tópicos por assunto, com formato e formulário próprios.
- **Formulário de categoria:** modelo em YAML que pede informações mínimas antes de abrir o tópico.
- **Moderação:** ação de organização do espaço, distinta da decisão de conduta.
- **Tópico fixado:** discussão mantida no topo da categoria.

## Referências

- [Governança](GOVERNANCE.md)
- [Mantenedores](MAINTAINERS.md)
- [Escada de contribuição](CONTRIBUTOR_LADDER.md)
- [Código de conduta](CODE_OF_CONDUCT.md)
- [Segurança da comunidade](COMMUNITY_SAFETY.md)
- [Suporte](SUPPORT.md)
- [Encontros mensais abertos](ENCONTROS.md)
- [Diário público de avanços](DEVLOG.md)
- [Como ajudar em 30 minutos](SUPPORT.md#como-ajudar-em-30-minutos)
