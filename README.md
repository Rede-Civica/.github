# Arquivos de saúde da organização

Este repositório reúne os arquivos públicos que valem para toda a organização Rede Cívica: governança, conduta, suporte, segurança, política de IA, guia de contribuição, espaço de comunidade, métricas e templates de issue e pull request.

O perfil da organização é [`profile/README.md`](profile/README.md) e aparece em [github.com/Rede-Civica](https://github.com/Rede-Civica).

## Comece por aqui

- [Arquitetura](ARCHITECTURE.md): repositórios, fluxo de eventos e onde mexer.
- [Guia de contribuição](CONTRIBUTOR_HANDBOOK.md): do zero ao primeiro pull request em um dia.
- [Governança](GOVERNANCE.md): papéis, decisões e caminho até a fundação.
- [Suporte](SUPPORT.md): canais, prazos e escopo.
- [Código de conduta](CODE_OF_CONDUCT.md): convivência, relato e apelação.
- [Segurança](SECURITY.md): relato de vulnerabilidade.

## Documentos

| Arquivo | Função |
|---|---|
| [`ARCHITECTURE.md`](ARCHITECTURE.md) | Mapa dos repositórios, fluxo de eventos e onde mexer. |
| [`GOVERNANCE.md`](GOVERNANCE.md) | Papéis, decisões, propostas públicas de mudança, veto e caminho até a fundação. |
| [`MAINTAINERS.md`](MAINTAINERS.md) | Quem mantém, área, disponibilidade e contato. |
| [`CONTRIBUTOR_LADDER.md`](CONTRIBUTOR_LADDER.md) | Níveis de contribuição, critérios, tempo e evidência. |
| [`SUPPORT.md`](SUPPORT.md) | Canais, prazos, escopo e versões suportadas. |
| [`ROADMAP.md`](ROADMAP.md) | Agora, próximo, depois e onde o projeto precisa de ajuda. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Normas, escopo, relato, aplicação e apelação. |
| [`COMMUNITY_SAFETY.md`](COMMUNITY_SAFETY.md) | Plano de incidente, prazos, medidas provisórias e registros. |
| [`AI_POLICY.md`](AI_POLICY.md) | Declaração de uso de IA, responsabilidade humana, agentes e feedback de modelo. |
| [`SECURITY.md`](SECURITY.md) | Canal, escopo, prazos e divulgação coordenada de vulnerabilidades. |
| [`CONTRIBUTOR_HANDBOOK.md`](CONTRIBUTOR_HANDBOOK.md) | Setup, primeiro pull request, gates, revisão e CLA em linguagem simples. |
| [`DISCUSSIONS.md`](DISCUSSIONS.md) | Categorias, regras e moderação das Discussões. |
| [`ENCONTROS.md`](ENCONTROS.md) | Formato, pauta e notas dos encontros mensais abertos. |
| [`DEVLOG.md`](DEVLOG.md) | Modelo do diário público de avanços. |
| [`METRICS.md`](METRICS.md) | Definições, primeira medição, metas e relatório mensal de saúde da comunidade. |
| [`CLA.md`](CLA.md) | Acordo de Licença de Contribuição. |
| [`TRADEMARK.md`](TRADEMARK.md) | Política de uso do nome e do logo. |
| [`PULL_REQUEST_TEMPLATE.md`](PULL_REQUEST_TEMPLATE.md) | Checklist padrão de pull request. |
| [`ISSUE_TEMPLATE/`](ISSUE_TEMPLATE/) | Templates de issue da organização. |
| [`profile/README.md`](profile/README.md) | Perfil público da organização. |

## Configuração e automação

| Arquivo | Função |
|---|---|
| `package.json` e `package-lock.json` | Dependências e comandos de verificação. |
| `.nvmrc` | Versão do Node.js usada no desenvolvimento e no CI. |
| `.markdownlint-cli2.jsonc` | Regras do markdownlint. |
| `.markdown-link-check.json` | Configuração do verificador de links. |
| `.github/workflows/` | Verificação de markdown e links, gitleaks, CodeQL e OpenSSF Scorecard. |
| `.github/dependabot.yml` | Atualizações de dependências. |
| `.github/DISCUSSION_TEMPLATE/` | Formulários das categorias de Discussão. |
| `ots/` | Provas de anterioridade das tags. |

## Verificação

O repositório usa Node.js 22.23.4.

```bash
npm ci
npm run verificar
```

O comando roda markdownlint e markdown-link-check em todo o markdown. O workflow [`verificacao.yml`](.github/workflows/verificacao.yml) repete a verificação em pull request e push na `main`, junto com `npm audit`.

## Licença

As licenças de código, texto e marca estão no [perfil da organização](https://github.com/Rede-Civica). O texto de governança segue CC BY-SA 4.0. A automação de verificação segue AGPL-3.0. A marca segue [`TRADEMARK.md`](TRADEMARK.md).
