# Política de segurança — Rede Cívica

Este arquivo vale para todos os repositórios da organização. Ele define como relatar vulnerabilidades, o que está no escopo e o que esperar.

## Como relatar

1. Preferência: Private Vulnerability Reporting no repositório afetado, no menu Security. O canal fica ativo quando o repositório é público.
2. Alternativa: e-mail para contato@redecivica.com.br, com o assunto `Segurança`.
3. Não abra issue pública com detalhe de exploração.

O site publica o mesmo contato em [`/.well-known/security.txt`](https://docs.redecivica.com.br/.well-known/security.txt), no formato definido pela RFC 9116.

Inclua no relato:

- Componente e versão afetada.
- Passos para reproduzir.
- Impacto estimado.
- Ambiente e configuração relevante.
- Prova de conceito, se houver.
- Se o problema já foi divulgado a terceiros.

Não inclua dado pessoal real, credencial ativa ou conteúdo de terceiros. Use dados de teste.

## Interface com a segurança da comunidade

Se o relato envolver ameaça, assédio, exposição de dados pessoais ou ataque coordenado, siga também o [plano de segurança da comunidade](COMMUNITY_SAFETY.md). Quando houver componente técnico, os dois fluxos correm em paralelo, com acesso restrito.

## Escopo

Está no escopo:

- Código da API, do web, do serviço de inferência e do site.
- Configuração de infraestrutura e workflows.
- Dependências e cadeia de build.
- Falha de autenticação, autorização, injeção, XSS, CSRF, SSRF, path traversal, upload e rate limit.
- Exposição de dado pessoal, falha de isolamento entre colônias e quebra de controle de acesso.
- Falha que permita manipulação de ranking, validação social, moderação ou conclusão de demanda.

Está fora do escopo:

- Valores de desenvolvimento documentados como de uso local.
- Dúvida de uso ou configuração. Use as issues comuns.
- Infraestrutura de terceiros, provedor de nuvem ou rede local.
- Engenharia social sem componente técnico.
- Relato sem passos de reprodução.
- Teste que acesse, altere ou exponha dado de terceiros.

## Prazos

- Confirmação de recebimento: até 5 dias úteis.
- Triagem e classificação inicial: até 10 dias úteis.
- Atualização do caso: a cada 10 dias úteis enquanto estiver aberto.
- Correção: depende da severidade e da complexidade.
- Divulgação coordenada: prazo alvo de 90 dias, salvo acordo diferente com quem relatou.

O projeto não garante recompensa financeira por relato.

## Divulgação coordenada

- Não divulgue o problema antes do acordo.
- O projeto coordena a correção e a data de publicação do advisory.
- O crédito é dado a quem relatou, salvo pedido de anonimato.
- Segredo exposto em histórico exige rotação imediata da credencial. Apagar o commit não resolve.

## Safe harbor

Se você seguir esta política, agir de boa-fé, acessar apenas o necessário para demonstrar a falha e não causar dano a terceiros, o projeto não tomará ação legal contra você por causa do relato.

Esta declaração não autoriza acesso a dado pessoal, interrupção de serviço, alteração de dado ou exploração além do mínimo necessário para demonstrar a falha. Ela não cria relação de cliente, contrato ou garantia.

## Versões suportadas

| Versão | Suporte |
|---|---|
| `main` | Sim, é a referência atual |
| `develop` | Correções direcionadas |
| Releases públicas | Nenhuma release pública até esta publicação |

O projeto não publica releases versionadas antes da produção. Correções entram primeiro em `develop` e seguem para `main`.

## Repositórios

Cada repositório de código publica o próprio `SECURITY.md` quando fica público. Até lá, este arquivo é o canal da organização.

- [mvp-api](https://github.com/Rede-Civica/mvp-api/blob/main/SECURITY.md)
- [mvp-web](https://github.com/Rede-Civica/mvp-web/blob/main/SECURITY.md)
- [mvp-inferencia](https://github.com/Rede-Civica/mvp-inferencia/blob/main/SECURITY.md)
- [mvp-docs](https://github.com/Rede-Civica/mvp-docs/blob/main/SECURITY.md)

Os links dos repositórios privados passam a resolver quando os repositórios ficarem públicos. Enquanto isso, use o e-mail acima.

## Contato

- E-mail: contato@redecivica.com.br.
- Assunto: `Segurança`.
- Não envie segredo, token ou dado pessoal por issue pública.
