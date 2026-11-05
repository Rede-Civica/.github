# Guia de contribuição

Este guia leva uma pessoa do zero ao primeiro pull request em um dia. Ele cobre o caminho comum aos repositórios da organização. As regras técnicas de cada repositório estão no `AGENTS.md` e no `CONTRIBUTING.md` do próprio repositório.

O projeto está em alpha fechado. O repositório `.github` é público. O `docs` e os repositórios de código abrem no lançamento de fevereiro de 2027. Enquanto um repositório estiver privado, a participação acontece nas [Discussões](https://github.com/Rede-Civica/.github/discussions) e nas issues públicas da organização.

## Antes de começar

- Leia a [Carta Social](SOCIAL_CHARTER.md), o [código de conduta](CODE_OF_CONDUCT.md) e o [plano de segurança da comunidade](COMMUNITY_SAFETY.md).
- Leia a [governança](GOVERNANCE.md), a [escada de contribuição](CONTRIBUTOR_LADDER.md) e o [roadmap](ROADMAP.md).
- Saiba onde pedir ajuda e os prazos no [SUPPORT.md](SUPPORT.md).
- Ative a autenticação em dois fatores na conta do GitHub.
- Você não precisa concordar com a tese do projeto para contribuir de boa-fé. O limite é o código de conduta.

## Escolha o seu caminho

| Caminho | Repositório | Branch base | Precisa de | Primeiro comando |
|---|---|---|---|---|
| Governança e comunidade | `.github` | `main` | Node.js 22.23.4 | `npm ci && npm run verificar` |
| Documentação e livro | `docs` | `master` | Node.js 22.23.4 | `npm ci && npm run verificar` |
| Site de documentação | `mvp-docs` | `main` | Node.js 22.23.4 | `npm ci && npm test` |
| API | `mvp-api` | `develop` | Node.js 22.23.4 e Docker opcional | `npm ci && npm test` |
| Aplicativo web | `mvp-web` | `develop` | Node.js 22.23.4 | `npm ci && npm test` |
| Inferência | `mvp-inferencia` | `develop` | Python 3.12 e `uv` | `uv sync && uv run pytest` |

O Node.js é fixado em 22.23.4. Use `nvm use` na raiz do repositório. O Python é fixado em 3.12 e o `uv` cuida do ambiente e das dependências.

## Setup de 15 minutos

O setup mecânico leva cerca de 15 minutos. A leitura do `AGENTS.md` e do `CONTRIBUTING.md` leva mais tempo e é obrigatória antes do primeiro pull request.

1. Crie ou confirme a sua conta no GitHub.
2. Ative a autenticação em dois fatores.
3. Instale o Git.
4. Instale o Node.js 22.23.4 com `nvm`, ou o Python 3.12 com `uv`, conforme o caminho escolhido.
5. Faça fork do repositório para a sua conta, quando você não tiver permissão de escrita.
6. Clone o seu fork.
7. Adicione o repositório da organização como `upstream`.
8. Crie a branch a partir da base correta.
9. Instale as dependências.
10. Rode o primeiro check.
11. Leia o `AGENTS.md` e o `CONTRIBUTING.md`.
12. Escolha uma issue.

Exemplo para o repositório `.github`:

```bash
git clone https://github.com/<seu-usuario>/.github.git
cd .github
git remote add upstream https://github.com/Rede-Civica/.github.git
git fetch upstream
git switch -c docs/minha-primeira-contribuicao upstream/main
npm ci
npm run verificar
```

Para `docs`, troque a base para `upstream/master`. Para `mvp-api`, `mvp-web` e `mvp-inferencia`, troque a base para `upstream/develop`.

## Seu primeiro PR em 1 dia

O caminho abaixo cabe em um dia de 4 a 6 horas. Se você tiver menos tempo, escolha uma tarefa de 30 minutos.

### 1. Escolha uma tarefa

- Abra as issues com o label [`good first issue`](https://github.com/Rede-Civica/.github/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).
- Leia o contexto, o critério de aceite, os arquivos prováveis e o tempo estimado.
- Comente na issue que você vai trabalhar nela. Isso evita trabalho duplicado.
- Se a issue não estiver clara, pergunte antes de começar.

### 2. Prepare o ambiente

- Siga o setup de 15 minutos.
- Leia o `AGENTS.md` do repositório por inteiro.
- Leia o `CONTRIBUTING.md` do repositório.
- Rode os gates antes de mudar qualquer coisa. O ambiente precisa estar verde.

### 3. Faça a mudança

- Mantenha o escopo pequeno. Um pull request resolve um problema.
- Siga o estilo do repositório.
- Atualize testes e documentação quando a mudança exigir.
- Não inclua dado pessoal, segredo ou credencial.
- Se usar IA, declare no pull request e revise o resultado. A pessoa humana responde pelo conteúdo.

### 4. Rode os gates

- Corrija o que falhar antes de abrir o pull request.
- Se um check falhar por instabilidade de rede, tente de novo.
- Se continuar bloqueado por mais de 30 minutos, peça ajuda na issue.

### 5. Abra o pull request

- Use o template da organização.
- Descreva o problema, a solução e o que foi testado.
- Vincule a issue com `Fixes #<número>`.
- Aceite o CLA quando o CLA Assistant pedir.
- Marque o pull request como rascunho se ainda estiver trabalhando.

### 6. Acompanhe a revisão

- A primeira resposta humana sai em até 5 dias úteis.
- Responda aos comentários e envie novos commits na mesma branch.
- Não faça force push depois de uma revisão, salvo pedido do revisor.
- O merge é feito por um mantenedor, depois da aprovação e dos checks verdes.

### Exemplo real

O commit [`0357167`](https://github.com/Rede-Civica/.github/commit/0357167) alterou o `profile/README.md` para apontar os links das Discussões ativas. A mudança foi pequena, em um arquivo, sem código, com o link verificado antes do merge. É um bom modelo de primeiro pull request: um problema claro, uma alteração objetiva e os gates verdes.

### Checklist do primeiro PR

- [ ] Escolhi uma issue e comentei que vou trabalhar nela.
- [ ] Li o `AGENTS.md` e o `CONTRIBUTING.md` do repositório.
- [ ] Criei a branch a partir da base correta.
- [ ] Mantive a mudança pequena e com um propósito.
- [ ] Atualizei testes e documentação quando necessário.
- [ ] Rodei os gates e eles estão verdes.
- [ ] Aceitei o CLA no pull request.
- [ ] Preenchi o template e vinculei a issue.
- [ ] Não incluí segredo, credencial ou dado pessoal.
- [ ] Respondi à revisão.

## Fluxo de pull request

1. **Issue primeiro.** Abra uma issue descrevendo o problema ou a proposta. Mudança sem issue anterior pode ser rejeitada. Correção de erro de digitação, link quebrado ou formatação sem mudança de conteúdo dispensa a issue.
2. **Fork e branch.** Faça fork, crie a branch a partir da base correta e use um nome em inglês kebab-case. Exemplos: `fix/link-quebrado`, `docs/guia-primeiro-pr`.
3. **Commits.** Use Conventional Commits em português, com commits atômicos. Exemplo: `docs: corrigir link do guia de contribuição`.
4. **CLA.** Aceite o [CLA](CLA.md) no pull request. O aceite cobre as contribuições presentes e futuras.
5. **Pull request.** Preencha o template, descreva o problema e a solução, vincule a issue e informe o que foi testado.
6. **Gates.** Rode os checks do repositório e deixe o CI verde.
7. **Revisão.** Um mantenedor revisa. O merge acontece depois da aprovação e dos checks verdes.
8. **Reconhecimento.** A contribuição entra no histórico, nas notas de marco e na lista de contribuidores, com consentimento.

## Gates por repositório

| Repositório | Gates |
|---|---|
| `.github` | `npm run verificar` |
| `docs` | `npm run verificar` |
| `mvp-docs` | `npm run lint`, `npm run typecheck`, `npm run format:check`, `npm run test`, `npm run build` |
| `mvp-api` | `npm run lint`, `npm run typecheck`, `npm run format:check`, `npm run test` |
| `mvp-web` | `npm run lint`, `npm run typecheck`, `npm run format:check`, `npm run test` |
| `mvp-inferencia` | `uv run ruff check`, `uv run ruff format --check`, `uv run pyright`, `uv run pytest` |

O `mvp-api`, o `mvp-web` e o `mvp-inferencia` têm cobertura mínima travada. Não reduza o piso. O `mvp-docs` tem testes de transformação, navegação, rodapé e integridade, sem piso de cobertura.

Para rodar um teste isolado:

```bash
npm test -- caminho/do/arquivo.spec.ts
uv run pytest tests/test_auth.py -q
```

## O que esperar da revisão

- Primeira resposta humana em até 5 dias úteis.
- Revisão semanal, salvo bloqueio declarado no pull request.
- O revisor pode pedir mudanças, testes ou documentação.
- Não há prazo garantido para merge. O merge depende da revisão e dos checks.
- O pull request parado há 30 dias sem atividade recebe um comentário. Se continuar parado por 7 dias, pode ser fechado. A pessoa pode reabrir quando retomar.
- O label `blocked` indica que o pull request depende de outra mudança ou de uma decisão.
- O label `needs-triage` indica que a issue ainda não foi classificada.
- O mantenedor faz o merge. A pessoa que contribuiu não faz o próprio merge, salvo quando já tem permissão de mantenedor.

## CLA em linguagem simples

O CLA é o [Acordo de Licença de Contribuição](CLA.md). Ele permite que o projeto distribua o código e o texto que você envia. O texto jurídico é o do `CLA.md`. Esta seção é um resumo explicativo e não altera o contrato. As [perguntas frequentes](CLA_FAQ.md) estão no arquivo próprio.

### Perguntas frequentes sobre o CLA

**Por que existe.** O projeto distribui o código sob AGPL-3.0-only e o texto sob CC BY-SA 4.0. O CLA registra que você tem o direito de enviar a contribuição e que o projeto pode distribuir o que você enviou.

**O que você mantém.** Você continua com o direito autoral da sua contribuição e pode usá-la para qualquer outro fim.

**O que você concede.** Você concede ao projeto uma licença perpétua, mundial, não exclusiva, gratuita, irrevogável e com direito de sublicenciar, limitada à distribuição sob a AGPL-3.0-only. A licença cobre reproduzir, preparar obras derivadas, exibir, executar, sublicenciar e distribuir a contribuição.

**O que o projeto não pode fazer.** O CLA v2.0 é AGPL-only. O projeto não pode relicenciar a sua contribuição sob termos proprietários, vender uma licença comercial do seu código ou incluir a contribuição em versão fechada. A [Carta Social](SOCIAL_CHARTER.md) registra o compromisso e vincula a marca e a fundação.

**Compromisso de licença.** O código oficial permanece AGPL-3.0-only e o texto permanece CC BY-SA 4.0. Mudança de licença exige proposta pública de mudança, 30 dias de comentários, aprovação do fundador e consulta aos owners de continuidade, conforme a seção "Licença e compromissos" da [governança](GOVERNANCE.md#licença-e-compromissos). A licença só pode mudar para outra licença copyleft que preserve as mesmas liberdades.

**Uso comercial.** O projeto não vende licença de software e não distribui lucro. Terceiros podem usar o código sob a AGPL, inclusive para prestar serviço comercial, desde que mantenham a versão derivada aberta e ofereçam o código-fonte a quem usa o serviço pela rede.

**Como aceitar.** O CLA Assistant pede o aceite no primeiro pull request. Comente a frase indicada. O aceite cobre as contribuições presentes e futuras.

**Contribuição sem CLA.** Você pode abrir issue, participar das Discussões, revisar e sugerir documentação sem assinar o CLA. O merge de código ou texto exige o aceite.

**Pessoa jurídica.** A Parte II do CLA vale para quem contribui em nome de uma empresa ou entidade. A entidade informa as pessoas autorizadas por e-mail para contato@redecivica.com.br.

**Uso de IA.** A pessoa que assina o CLA responde pelo conteúdo, com ou sem assistência de ferramenta. Declare o uso de IA no pull request. A política completa está em [AI_POLICY.md](AI_POLICY.md).

## Uso de IA

A política completa está em [AI_POLICY.md](AI_POLICY.md). Resumo:

- Declare no pull request quando usar IA para código, texto, teste, imagem ou revisão.
- Diga quais partes foram assistidas e qual ferramenta foi usada.
- Revise o resultado antes de enviar. A pessoa humana responde pelo conteúdo.
- Não use IA para abrir ou mergear pull request de forma autônoma.
- Não envie texto legal, conceitual ou de governança gerado por IA sem revisão humana.
- Não use IA para reproduzir obra de terceiros sem licença.
- Erro de modelo tem canal de feedback na categoria Feedback de modelo das Discussões.

## Labels

| Label | Significado |
|---|---|
| `good first issue` | Tarefa pequena, com contexto e critério de aceite, para a primeira contribuição. |
| `help wanted` | A tarefa precisa de ajuda e pode ter mais de uma pessoa interessada. |
| `docs` | Mudança em documentação, guia, referência ou texto. |
| `bug` | Comportamento incorreto reproduzível. |
| `enhancement` | Melhoria ou funcionalidade nova. |
| `question` | Dúvida sobre uso, contrato ou modelo. |
| `ai-assisted` | A contribuição usou assistência de IA e a declaração está no pull request. |
| `needs-triage` | A issue ainda não foi classificada pela triagem. |
| `blocked` | A tarefa depende de outra mudança ou de uma decisão. |
| `mentor` | A issue tem uma pessoa mentora indicada. |

## Triagem semanal e prazos

A triagem acontece uma vez por semana, em 30 minutos, na segunda-feira. Feriados podem deslocar a triagem para o próximo dia útil.

Na triagem, os mantenedores:

1. leem as issues e os pull requests novos;
2. aplicam labels, incluindo `needs-triage`, `bug`, `docs`, `enhancement` e `good first issue`;
3. respondem à primeira mensagem em até 5 dias úteis;
4. pedem informação que falta;
5. fecham duplicata com link para a issue original;
6. indicam mentor nas tarefas de primeira contribuição;
7. atualizam o roadmap quando a demanda muda de prioridade.

O pull request parado há 30 dias sem atividade recebe um comentário. Se continuar parado por 7 dias, pode ser fechado com uma nota. A pessoa pode reabrir quando retomar.

## Reconhecimento

O projeto reconhece contribuição de código, documentação, design, teste, tradução, triagem, revisão e comunidade.

- **All Contributors.** O crédito aparece no pull request e nas notas de marco, com consentimento.
- **Notas de marco.** Cada marco de desenvolvimento lista as contribuições por área.
- **Hall da fama.** A lista pública de contribuidores será publicada no [perfil da organização](https://github.com/Rede-Civica) quando houver o primeiro ciclo de contribuições externas. Ninguém entra sem consentimento.
- **Mantenedores e revisores.** A lista nominal fica em [MAINTAINERS.md](MAINTAINERS.md).
- **Sem ranking por volume.** O reconhecimento considera o efeito no projeto, não a quantidade de commits.

## Onde pedir ajuda

| Assunto | Canal |
|---|---|
| Dúvida de contribuição, instalação ou uso | [Discussões, categoria Ajuda](https://github.com/Rede-Civica/.github/discussions/categories/ajuda) |
| Bug reproduzível | Issue com o template de bug |
| Proposta com escopo | Issue com o template de funcionalidade |
| Suporte e prazos | [SUPPORT.md](SUPPORT.md) |
| Conduta | [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) e [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md) |
| Vulnerabilidade | [SECURITY.md](SECURITY.md) |
| Assunto institucional | contato@redecivica.com.br |

Não use mensagem privada para pedido de suporte. A conversa pública fica registrada e ajuda outras pessoas.

## Problemas comuns

**O `npm ci` falha.** Confira `node --version`. O valor precisa ser 22.23.4. Rode `nvm use` na raiz do repositório e tente de novo.

**O link check falha com 403 ou 429.** O GitHub pode limitar requisições. Espere alguns minutos e rode de novo. Se o link estiver quebrado, corrija o endereço.

**O build do `mvp-docs` falha.** O build lê o repositório `docs` em `../docs` ou no caminho de `DOCS_ORIGEM`. Confira se a origem existe e se a sincronização rodou.

**O `uv sync` falha.** Confira a versão do Python com `python --version`. O projeto usa 3.12. Rode `uv sync` de novo depois de corrigir.

**O CLA Assistant não aparece.** Verifique se o pull request está aberto no repositório da organização e se o seu usuário está identificado. Se a conta for corporativa, use a Parte II do CLA.

**Não tenho permissão para enviar a branch.** Faça fork e abra o pull request a partir do fork. O fluxo está na seção "Fluxo de pull request".

**Estou bloqueado há mais de 30 minutos.** Comente na issue ou abra uma dúvida na categoria Ajuda. Diga o comando, o erro completo e o que já tentou.

## Glossário

- **Pull request (PR).** Pedido para incorporar uma mudança a um repositório.
- **Issue.** Registro público de bug, proposta, tarefa ou dúvida.
- **Fork.** Cópia do repositório na sua conta, usada para propor mudanças sem permissão de escrita.
- **Branch.** Linha de trabalho separada dentro do repositório.
- **Commit.** Registro de uma mudança, com mensagem.
- **Merge.** Incorporação de uma branch ao ramo principal.
- **Revisão.** Leitura técnica da mudança por outra pessoa, com comentários e aprovação.
- **Triagem.** Classificação de issues e pull requests com labels, prioridade e encaminhamento.
- **Label.** Etiqueta que classifica uma issue ou pull request.
- **Mentor.** Pessoa que acompanha uma tarefa de primeira contribuição.
- **Gate.** Verificação automática que precisa passar antes do merge.
- **Lint.** Verificação de estilo e de erros simples no código ou no markdown.
- **Typecheck.** Verificação de tipos do TypeScript ou do Python.
- **Cobertura.** Percentual do código exercitado pelos testes.
- **CLA.** Acordo de Licença de Contribuição.
- **AGPL-3.0-only.** Licença do código, com copyleft forte para serviços de rede.
- **CC BY-SA 4.0.** Licença do texto, com atribuição e compartilhamento na mesma licença.
