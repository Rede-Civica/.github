# Rede Cívica

Infraestrutura cívica digital para governança social. Cidadãos registram demandas do território. O sistema categoriza e prioriza por parâmetros públicos. Conselheiros sorteados acompanham a execução de forma rastreável.

## Repositórios

- [`mvp-api`](https://github.com/Rede-Civica/mvp-api): back-end NestJS. Monolito modular "O Formigueiro", orientado a eventos. AGPL-3.0.
- [`mvp-web`](https://github.com/Rede-Civica/mvp-web): front-end React, PWA map-first. AGPL-3.0.
- [`mvp-inferencia`](https://github.com/Rede-Civica/mvp-inferencia): serviço Python/FastAPI de inferência de IA self-hosted (imagem, áudio e texto), consumido pela API pela rede interna. AGPL-3.0.
- [`docs`](https://github.com/Rede-Civica/docs): livro, especificações de software, tutoriais, guias e referências. CC BY-SA 4.0.
- [`mvp-docs`](https://github.com/Rede-Civica/mvp-docs): site público de documentação, em [`docs.redecivica.com.br`](https://docs.redecivica.com.br). AGPL-3.0.

## Licença

Todo o código é [AGPL-3.0](https://www.gnu.org/licenses/agpl-3.0.html). Copyleft forte para serviços de rede.

O livro e a documentação são [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Compartilhamento e adaptação livres, com atribuição e a mesma licença.

O nome e o logo Rede Cívica são marca do projeto. A licença do código não concede direito de uso da marca. A política está em [`TRADEMARK.md`](https://github.com/Rede-Civica/.github/blob/main/TRADEMARK.md).

## Governança

A decisão final é do fundador até a constituição da fundação. A governança publica papéis, prazos, propostas públicas de mudança, veto e o caminho até a fundação.

- [Governança](https://github.com/Rede-Civica/.github/blob/main/GOVERNANCE.md)
- [Mantenedores](https://github.com/Rede-Civica/.github/blob/main/MAINTAINERS.md)
- [Escada de contribuição](https://github.com/Rede-Civica/.github/blob/main/CONTRIBUTOR_LADDER.md)
- [Roadmap](https://github.com/Rede-Civica/.github/blob/main/ROADMAP.md)
- [Suporte](https://github.com/Rede-Civica/.github/blob/main/SUPPORT.md)
- [Código de conduta](https://github.com/Rede-Civica/.github/blob/main/CODE_OF_CONDUCT.md)
- [Segurança](https://github.com/Rede-Civica/.github/blob/main/SECURITY.md)

## Como começar

O site [docs.redecivica.com.br](https://docs.redecivica.com.br) publica o livro, os tutoriais, os guias práticos e a referência.

- Entender o modelo: [livro Rede Cívica](https://docs.redecivica.com.br/rede-civica/) e [`rede_civica.md`](https://github.com/Rede-Civica/docs/blob/master/rede_civica.md).
- Rodar o projeto: [tutorial de execução local](https://docs.redecivica.com.br/tutoriais/rodando-o-projeto-localmente/).
- Contribuir: leia a [escada de contribuição](https://github.com/Rede-Civica/.github/blob/main/CONTRIBUTOR_LADDER.md) e o [guia de suporte](https://github.com/Rede-Civica/.github/blob/main/SUPPORT.md).
- Contribuir com a documentação: [como editar a documentação](https://docs.redecivica.com.br/como-editar-a-documentacao/).
- Contribuir com código: os repositórios abrem quando os critérios de segurança estiverem fechados. A escada e o guia de suporte valem desde já.
- Dúvidas e suporte: [issues da organização](https://github.com/Rede-Civica/.github/issues).
- Vulnerabilidades: [`SECURITY.md`](https://github.com/Rede-Civica/.github/blob/main/SECURITY.md).
- [Como ajudar em 30 minutos](https://github.com/Rede-Civica/.github/blob/main/SUPPORT.md#como-ajudar-em-30-minutos).

### Trilha de aprendizagem do mapa

Para quem quer entender a camada de mapa, do dado ao render, na ordem:

1. Fundamentos: [Mapas e tiles: como funcionam](https://github.com/Rede-Civica/docs/blob/master/mapa_e_tiles.md) no repo `docs`. Conceitos de tile e zoom e formatos de dado, com o glossário e as fontes na [referência de mapas e tiles](https://github.com/Rede-Civica/docs/blob/master/referencia_mapas_e_tiles.md).
2. Geração: [scripts/tiles](https://github.com/Rede-Civica/mvp-api/tree/main/scripts/tiles) no repo `mvp-api`. Como a camada base é gerada a partir do OpenStreetMap, dos prédios da Microsoft, da cobertura vegetal da Overture e do contexto dos vizinhos da América do Sul.
3. Consumo: seção "Mapa — como a camada base funciona" no [README do mvp-web](https://github.com/Rede-Civica/mvp-web#readme). Como o app serve e renderiza os tiles.

## Status

Alpha fechado. Beta aberto previsto para 2027. O aplicativo opera com dados de teste e convidados. Consulte a [página de estado do projeto](https://docs.redecivica.com.br/estado-do-projeto/).
