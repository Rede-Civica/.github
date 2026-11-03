# Segurança da comunidade

Este documento é o plano de aplicação do [código de conduta](CODE_OF_CONDUCT.md). Ele descreve como um relato entra, é triado, investigado e decidido, quais medidas podem ser tomadas, como funciona a apelação, o que fica registrado e como o projeto se comunica.

O objetivo é responder com segurança e devido processo. O plano existe para conflito real, não para um cenário ideal.

## Princípios

1. **Segurança primeiro.** Risco à integridade física tem prioridade sobre qualquer outra consideração.
2. **Devido processo.** A pessoa acusada sabe do que é acusada. A pessoa que relata recebe resposta. As duas podem apresentar sua versão.
3. **Proporcionalidade.** A medida responde ao dano, ao contexto e ao histórico. O mesmo fato pode receber medida diferente conforme o contexto.
4. **Confidencialidade.** O caso fica restrito a quem precisa conhecê-lo. O público recebe apenas o agregado.
5. **Registro.** Toda etapa relevante é registrada, com data, decisão e fundamento.
6. **Responsabilidade humana.** Nenhuma ferramenta decide o caso. Uma pessoa responde pela triagem, pela investigação e pela decisão.
7. **Sem retaliação.** Relatar, testemunhar ou participar da apuração não pode gerar prejuízo.
8. **Aprendizado.** Cada caso fechado alimenta revisão do código, do plano e da moderação.

## Papéis

| Papel | Responsabilidade |
|---|---|
| Respondedor | Recebe o relato, faz a triagem, investiga e decide |
| Respondedor de apelação | Revisa a decisão quando não participou do caso |
| Advisor externo | Pessoa conselheira externa que decide quando há conflito, risco elevado ou falta de respondedor livre |
| Fundador | Responde pela segurança da organização até a fundação |
| Moderador de comunidade | Aplica regras de espaço e encaminha caso de conduta ao respondedor |
| Owner de segurança | Trata o componente técnico quando o caso envolve informação, conta ou vazamento |

Os respondedores nominais estão em [MAINTAINERS.md](MAINTAINERS.md). O projeto mantém dois postos. Enquanto a segunda vaga estiver aberta, o fundador responde e um advisor externo decide quando o fundador estiver envolvido.

O moderador não decide caso de conduta. Ele contém o dano imediato no espaço, preserva evidência e encaminha o relato ao respondedor.

## Entrada

O relato entra por dois canais:

- e-mail para `contato@redecivica.com.br`, com o assunto `Conduta`;
- [formulário de relato](mailto:contato@redecivica.com.br?subject=Relato%20de%20conduta&body=O%20que%20aconteceu%3A%0A%0AQuando%3A%0A%0AOnde%3A%0A%0AQuem%20participou%3A%0A%0ATestemunhas%3A%0A%0AEvidencias%3A%0A%0ARisco%20imediato%3A%0A%0AConflito%20de%20interesse%3A%0A%0AContato%20preferido%3A), que abre o cliente de e-mail com os campos mínimos.

O relato deve trazer o que aconteceu, quando, onde, quem participou, testemunhas, evidências e risco imediato. O relato pode ser anônimo. O anonimato limita a apuração, mas o caso é registrado e triado com o que houver.

A confirmação de recebimento sai em até 3 dias úteis. Se o relato estiver incompleto, a confirmação pede o que falta e explica o que pode ser feito sem a informação.

Em risco imediato, a pessoa deve procurar primeiro o serviço de emergência local. O projeto não é serviço de emergência e não substitui polícia, defesa civil ou atendimento de saúde.

## Triagem

A triagem classifica o risco e define a prioridade. P0 é o nível mais grave e P3 é o mais leve. A classificação pode mudar durante o caso.

| Nível | Exemplos | Prazo de triagem | Ação inicial |
|---|---|---|---|
| P0 | Ameaça de violência iminente, doxxing com dado exposto, conteúdo sexual envolvendo menor, ataque coordenado em curso, risco à integridade física | Mesmo dia | Contenção imediata, segurança acionada, autoridade quando cabível |
| P1 | Assédio reiterado, ameaça sem iminência, discriminação, exposição de dados sem risco imediato, retaliação | 1 dia útil | Medida provisória se necessária, investigação prioritária |
| P2 | Insulto, conflito interpessoal, limite de espaço, divulgação de mensagem privada | 3 dias úteis | Orientação, mediação ou medida simples |
| P3 | Ruído, spam, desvio de tópico, conduta menor | 5 dias úteis | Orientação e registro |

Na triagem, o respondedor verifica:

- se existe risco à integridade física;
- se há dado pessoal exposto;
- se há menor de idade envolvido;
- se o comportamento é coordenado;
- se há relação de poder entre as pessoas;
- se o caso tem componente de segurança da informação;
- se o respondedor tem conflito de interesse.

Conflito declarado afasta o respondedor. O caso passa para o outro posto ou para o advisor externo.

## Medidas provisórias

Medida provisória existe para conter dano antes da decisão final. Ela não é punição definitiva.

São medidas provisórias:

- ocultar, remover ou limitar conteúdo;
- trancar issue, discussão ou sequência de mensagens;
- restringir interação de uma conta;
- suspender acesso a espaço, evento ou beta;
- pausar evento ou chamada;
- preservar evidência;
- contatar a plataforma para remoção;
- acionar autoridade quando houver risco iminente;
- oferecer acompanhamento à pessoa afetada.

A medida provisória é registrada com motivo, prazo e responsável. Ela é revista em até 5 dias úteis. Se o caso exigir mais tempo, a revisão é registrada com nova data.

## Investigação

A investigação segue estes passos:

1. Confirmar o conflito de interesse e definir o respondedor responsável.
2. Preservar evidência antes que conteúdo seja apagado ou editado.
3. Ouvir quem relatou, quem foi acusado e testemunhas, em separado.
4. Pedir informação complementar quando necessária.
5. Conferir o histórico público e os registros de moderação.
6. Consultar o advisor externo em caso P0, P1, conflito ou dúvida de procedimento.
7. Registrar a cronologia, as fontes e as lacunas.
8. Fechar a instrução e passar à decisão.

A investigação não exige que quem relatou confronte a pessoa acusada. A pessoa acusada tem direito de saber a acusação e de responder. Se não responder no prazo, a decisão segue com a evidência disponível.

Acesso a dado pessoal fica no mínimo necessário. Gravação de entrevista só acontece com consentimento. O material sensível não circula em issue, discussão ou pull request.

O padrão de prova é o conjunto de evidências tornar o relato mais provável que não. Não é necessário padrão criminal. Dúvida relevante é registrada na decisão.

## Decisão

A decisão inicial sai em até 10 dias úteis. O prazo pode ser prorrogado por até 10 dias úteis, com aviso a quem relatou e a quem foi acusado.

A decisão contém:

- resumo dos fatos considerados;
- regra do código de conduta aplicada;
- medida e prazo;
- condições de cumprimento;
- fundamento da medida;
- caminho e prazo de apelação.

A decisão é enviada às duas partes, com redação que protege dado pessoal. A pessoa que relatou recebe o resultado e o prazo de apelação. A pessoa acusada recebe a descrição da acusação e a medida.

Se não houver violação, o caso é encerrado com registro e resposta às partes. Se houver indício de crime, o projeto pode encaminhar à autoridade competente, sem substituir a decisão da pessoa lesada.

## Apelação

A apelação é pedida em até 10 dias úteis, por escrito, ao respondedor que não participou da decisão. Quando não houver respondedor livre, um advisor externo decide.

São motivos de apelação:

- evidência nova;
- erro de procedimento;
- medida desproporcional;
- conflito de interesse não declarado;
- fato relevante não considerado.

A apelação não suspende a medida, salvo decisão em contrário. A decisão da apelação sai em até 10 dias úteis e é final dentro do projeto. Depois da fundação, o conselho da fundação é a última instância interna.

## Registro e retenção

Cada caso recebe um identificador interno. O registro contém:

- data de entrada e canal;
- categoria e nível de risco;
- pessoas envolvidas, em campo restrito;
- conflito declarado e afastamento;
- medidas provisórias;
- evidências e fontes;
- decisão, medida e prazo;
- apelação e resultado;
- data de encerramento.

O registro fica em armazenamento restrito, com acesso limitado aos respondedores e ao advisor externo. Nenhum dado pessoal entra em issue, discussão, relatório público ou métrica.

O registro é mantido por dois anos após o encerramento. Depois disso, é eliminado ou anonimizado, salvo obrigação legal, medida permanente em vigor ou apelação pendente. Pedido de acesso, correção ou eliminação segue a [política de privacidade](https://docs.redecivica.com.br/politica-privacidade/), observados os prazos legais e a necessidade de manter o registro da medida.

## Comunicação

O projeto não comenta caso em aberto. A comunicação segue três regras:

- uma pessoa fala pelo projeto;
- nenhuma identidade é exposta;
- fato e suposição ficam separados.

Quando o caso tiver impacto público, a pessoa afetada é ouvida antes da declaração, quando possível. A declaração informa o que se sabe, o que não se sabe, o que será feito e quando haverá nova atualização.

## Interface com a segurança da informação

Se o caso envolver invasão de conta, vazamento de dados, doxxing com dado obtido de sistema, conteúdo ilegal ou ameaça com componente técnico, o owner de segurança entra no caso.

O fluxo de segurança segue [SECURITY.md](SECURITY.md). O fluxo de conduta segue este documento. Os dois correm em paralelo, com acesso restrito e sem publicar detalhe de exploração.

Medidas técnicas possíveis:

- rotacionar credencial exposta;
- revogar sessão ou token;
- preservar log e trilha de acesso;
- remover conteúdo e registrar hash;
- acionar a plataforma;
- acionar autoridade competente.

O caso de conduta não absorve o caso de segurança. Cada um tem registro próprio e comunicação própria.

## Procedimentos específicos

### Ameaça

1. Confirmar se há risco iminente à integridade física.
2. Orientar a pessoa ameaçada a procurar a polícia e preservar a evidência.
3. Preservar captura, link, horário e conta de origem.
4. Aplicar medida provisória de contenção.
5. Acionar a plataforma e, quando cabível, a autoridade.
6. Não responder à ameaça em público.
7. Registrar o caso como P0 e revisar em 24 horas.

### Doxxing

1. Preservar a evidência sem repetir o dado exposto.
2. Pedir remoção à plataforma e ao host do conteúdo.
3. Aplicar medida provisória contra a conta responsável.
4. Apoiar a pessoa afetada e orientar sobre risco digital e físico.
5. Acionar autoridade quando houver risco ou dado sensível.
6. Não publicar o dado em issue, discussão ou relatório.
7. Revisar a exposição em 24 horas e em 7 dias.

### Assédio coordenado

1. Identificar o padrão: contas, horários, mensagens e alvos.
2. Preservar a evidência e não amplificar o conteúdo.
3. Limitar interação, trancar a sequência e restringir contas.
4. Acionar a plataforma com a lista de contas e links.
5. Avisar as pessoas afetadas e combinar apoio.
6. Publicar declaração curta apenas se a amplitude exigir.
7. Monitorar por 72 horas e registrar a evolução.
8. Fazer retrospectiva em até 30 dias.

### Conteúdo ilegal

1. Não baixar, copiar ou encaminhar o conteúdo.
2. Remover o conteúdo do espaço do projeto.
3. Preservar apenas hash, metadados e data, quando a lei permitir.
4. Acionar a plataforma e a autoridade competente.
5. Não publicar detalhe do conteúdo.
6. Registrar o caso como P0 e comunicar as pessoas afetadas.
7. Revisar o acesso ao espaço e a moderação.

### Crise pública

Crise pública é o incidente com risco de dano, exposição ampla, cobertura de imprensa ou risco à continuidade do projeto.

1. Ativar o protocolo em até 24 horas.
2. Definir uma pessoa como porta-voz.
3. Preservar evidência e separar fato de suposição.
4. Ouvir as pessoas afetadas antes da declaração, quando possível.
5. Publicar a primeira declaração com o que se sabe, o que não se sabe e a próxima atualização.
6. Atualizar diariamente enquanto a crise estiver ativa.
7. Não debater com quem ataca em público.
8. Acionar apoio jurídico, plataforma e autoridade quando cabível.
9. Fazer retrospectiva pública em até 30 dias, sem dado pessoal.

## Simulação e revisão

A primeira simulação de mesa acontece em até 30 dias após a nomeação do segundo respondedor. Depois, uma vez por ano.

A simulação cobre, no mínimo:

- ameaça com componente de segurança;
- doxxing;
- assédio coordenado;
- conteúdo ilegal;
- crise pública.

Cada simulação produz registro de aprendizado e atualização deste plano. O plano é revisado também depois de todo caso P0.

## Transparência

O relatório anual de conduta segue o [código de conduta](CODE_OF_CONDUCT.md) e é publicado no repositório `.github`. Ele publica número de casos, tipos, medidas, tempos medianos, apelações e recomendações, sem identidade e sem detalhe de caso.

O projeto não compara casos com outros projetos. O relatório mede tendência e decisão.

## Glossário

- **Assédio coordenado:** várias pessoas ou contas agem juntas para intimidar, silenciar ou expulsar alguém.
- **Brigading:** mobilização de um grupo para inundar uma pessoa, issue ou discussão com mensagens, votos ou denúncias.
- **Doxxing:** exposição de dados pessoais sem consentimento, com risco de identificação ou dano.
- **Swatting:** acionamento falso de força policial contra alguém, com risco de violência.
- **Conteúdo ilegal:** material que viola a lei, como abuso sexual infantil, conteúdo íntimo não consensual, fraude e instrução para crime.

## Referências

- [Código de conduta](CODE_OF_CONDUCT.md)
- [Governança](GOVERNANCE.md)
- [Mantenedores e respondedores](MAINTAINERS.md)
- [Segurança da informação](SECURITY.md)
- [Suporte](SUPPORT.md)
- [Livro Rede Cívica](https://docs.redecivica.com.br/rede-civica/)
