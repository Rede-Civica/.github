# Dados da Rede Cívica

Este documento é um mapa das classes de dados do projeto. Ele não substitui a política de privacidade. O texto canônico continua na [Política de Privacidade](https://docs.redecivica.com.br/politica-privacidade/).

O ROPA (registro das operações de tratamento) e os registros de operação ficam privados e não são publicados. Este mapa não altera finalidade, base legal, retenção, consentimento ou qualquer operação de tratamento.

## Como ler

| Exposição | Significado |
|---|---|
| Público | Leitura sem login e reutilização sob a licença indicada. |
| Restrito | Acesso controlado por papel e finalidade. Não é base aberta e não tem licença de reutilização. |
| Protegido | Dado pessoal ou sensível sob a LGPD. Não tem licença aberta, mesmo quando uma parte aparece no aplicativo. |

## Classes de dados

| Classe | Exemplos | Exposição | Licença |
|---|---|---|---|
| Código | API, web, inferência, site, workflows | Público | AGPL-3.0-only |
| Texto e documentação | Livro, SDS, tutoriais, guias | Público | CC BY-SA 4.0 |
| Dados públicos agregados | Contagens, rankings, indicadores por unidade cívica | Público | CC BY 4.0, sujeita a revisão jurídica |
| Dados operacionais | Eventos, logs, moderação, histórico | Restrito | Não licenciado |
| Dados pessoais | Identidade, dispositivo, localização, mídia, áudio | Protegido | Não licenciado |
| Segredos | Chaves, tokens, senhas | Nunca público | Não licenciado |
| Pesos e modelos | Florence-2, Whisper, OPUS-MT, Qwen | Conforme licença do modelo | Licença própria de cada modelo |

## Dados públicos

### Código

O código dos repositórios da organização usa AGPL-3.0-only. A automação de verificação deste repositório também usa AGPL-3.0-only. O uso exige o cumprimento da licença, incluindo a oferta do código-fonte para quem interage com o serviço pela rede.

### Texto e documentação

O livro, os SDS, os tutoriais e os guias usam CC BY-SA 4.0. A reutilização exige atribuição e a mesma licença nas obras derivadas. O texto de governança deste repositório segue a mesma licença.

A marca não entra na licença do código nem do texto. O uso do nome e do logo segue o [TRADEMARK.md](TRADEMARK.md).

### Dados públicos agregados

Contagens, rankings, indicadores por unidade cívica e os resumos públicos derivados são publicados sob CC BY 4.0, sujeita a revisão jurídica. A licença cobre o conjunto agregado publicado, não os dados de origem. A agregação não pode permitir a reidentificação de uma pessoa.

O projeto não vende, aluga ou licencia dados pessoais. Não há publicidade, vigilância comercial ou uso de dado pessoal para treinar modelo de terceiro sem consentimento. O compromisso está na [Carta Social](SOCIAL_CHARTER.md).

A atribuição sugerida é "Rede Cívica, dados públicos agregados, CC BY 4.0", com link para a licença e indicação de alterações. A revisão jurídica pode ajustar a licença antes da publicação de uma base agregada. Se isso acontecer, o dado publicado e a licença mudam juntos.

Se o projeto publicar uma base geográfica completa derivada do OpenStreetMap, a licença será a ODbL, com a atribuição "© OpenStreetMap contributors". A ODbL fica reservada para esse caso. Os dados de mapa que já existem têm licenças próprias, descritas na [referência de mapas e tiles](https://docs.redecivica.com.br/referencia-mapas-e-tiles/).

### Pesos e modelos

Cada modelo tem licença própria. As fichas estão em [MODELS.md](MODELS.md). O projeto não relicencia pesos de terceiros. A atribuição de cada modelo está na referência pública de [licenças e atribuições](https://docs.redecivica.com.br/referencia-modelos-de-inferencia/#licenças-e-atribuições).

## Dados restritos

### Operação

Eventos, logs, filas, histórico de moderação e registros de segurança são restritos. O acesso segue papel e finalidade. O histórico público de uma demanda é uma projeção sanitizada, não o registro operacional bruto.

O registro de eventos é imutável por desenho. A transparência em camadas do livro explica a diferença entre o registro do processo, as visões agregadas e as análises. O registro imutável guarda o processo, não o conteúdo pessoal. O conteúdo pessoal fica em armazenamento próprio, referenciado por identificador. A [seção de transparência do livro](https://docs.redecivica.com.br/rede-civica/#transparência-e-sobrecarga-informacional) descreve o modelo.

### ROPA

O ROPA é mantido pelo controlador e fica à disposição da ANPD quando solicitado. Ele não é publicado. O registro descreve operações, finalidades, bases legais, categorias de titulares, categorias de dados, destinatários, transferências, retenção e medidas de segurança.

### Segredos

Chaves, tokens, senhas, credenciais e arquivos de ambiente com valor real nunca são públicos. O valor de desenvolvimento documentado como local não é segredo de produção. Segredo exposto em issue, pull request, log ou histórico exige rotação imediata. Apagar o commit não resolve.

## Dados protegidos

### Dados pessoais

Identidade, dispositivo, localização, texto, mídia e áudio são dados pessoais. A LGPD se aplica. A [Política de Privacidade](https://docs.redecivica.com.br/politica-privacidade/) descreve finalidade, base legal, retenção e direitos. O conteúdo de uma demanda pode aparecer no aplicativo, mas continua protegido e sem licença aberta. A exibição pública não autoriza a reutilização fora da rede.

| Dado | Onde aparece | Regra |
|---|---|---|
| Identificador anônimo do dispositivo | Restrito ao schema interno | Gerado no primeiro acesso. Não é publicado. |
| Localização aproximada | Aplicativo, quando o titular autoriza | No log de eventos, a localização é reduzida à precisão da unidade cívica, cerca de 1 km. |
| Texto, categoria, localização e mídia da demanda | Aplicativo, como conteúdo da demanda | O texto é escrito por quem publica. A mídia passa pela classificação automática e pela moderação. A exibição não é licença de reutilização. |
| Áudio da demanda e do relato do conselheiro | Restrito à auditoria | A transcrição é revisada pelo autor antes de publicar. O áudio nunca é publicado. |
| Nome e e-mail da conta | Restrito ao login opcional | Só entram quando o titular escolhe entrar com a conta Google. |
| Identificadores de ação social | Restrito ao schema interno | Servem para impedir repetição e excluir o autor das ações sobre o próprio registro. Não são publicados. |
| Dados do conselheiro | Registros internos e timeline pública revisada | Áudio restrito. O texto da atualização é revisado pelo conselheiro antes de publicar. |
| CNPJ e vínculo do representante | CNPJ autodeclarado e vínculo restrito | O CNPJ é aceito por formato e dígitos verificadores, sem consulta à Receita Federal. O vínculo não é publicado. |
| Sinais de rede | Restrito | O IP não é armazenado em banco, evento, log ou métrica. Ficam os sinais `ip_hospedagem` e `distancia_ip_gps_faixa`. |

### Direitos do titular

O titular pode pedir acesso, correção, eliminação, portabilidade e revogação do consentimento. O pedido entra pela tela "Meus dados" do aplicativo ou pelo contato do encarregado. A resposta sai em até 15 dias. O exercício dos direitos exige conta verificada. O usuário em modo anônimo pode gerar um novo identificador do aparelho a qualquer momento.

O contato do encarregado é contato@redecivica.com.br, somente para assuntos de proteção de dados.

## Dados pessoais em issue, pull request, exemplo e formulário

- Nunca inclua dado pessoal real, mídia de terceiros, credencial, token ou conteúdo confidencial.
- Use dado sintético ou de teste. Se precisar mostrar uma tela, tarje nome, e-mail, telefone, endereço, localização precisa, identificador e qualquer dado de terceiro.
- Se o caso exigir dado sensível, diga isso sem enviar o dado e peça um canal privado.
- Vulnerabilidade de segurança não entra em issue. O relato segue o [SECURITY.md](SECURITY.md).
- Relato de conduta não entra em issue. O canal e os prazos estão no [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) e no [COMMUNITY_SAFETY.md](COMMUNITY_SAFETY.md).
- Se um item contiver dado pessoal ou segredo, a triagem remove o conteúdo, avisa a pessoa por canal privado e registra o incidente. Segredo exposto exige rotação imediata.

O CLA Assistant registra o usuário, o nome e o e-mail da conta do GitHub e o número do pull request. A explicação está no [CLA_FAQ.md](CLA_FAQ.md).

## O que não muda

Este documento não altera a política de privacidade, o ROPA, a retenção, o consentimento ou qualquer operação de tratamento. Nenhum dado pessoal novo entra em README, issue, exemplo, formulário ou métrica. A política canônica continua na [Política de Privacidade](https://docs.redecivica.com.br/politica-privacidade/).

## Referências

- [Política de Privacidade](https://docs.redecivica.com.br/politica-privacidade/)
- [Transparência e sobrecarga informacional](https://docs.redecivica.com.br/rede-civica/#transparência-e-sobrecarga-informacional)
- [Referência de modelos de inferência](https://docs.redecivica.com.br/referencia-modelos-de-inferencia/)
- [Referência de mapas e tiles](https://docs.redecivica.com.br/referencia-mapas-e-tiles/)
- [MODELS.md](MODELS.md)
- [CLA_FAQ.md](CLA_FAQ.md)
- [AI_POLICY.md](AI_POLICY.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
