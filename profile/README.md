# Rede Cívica

Infraestrutura cívica digital para governança social. Cidadãos registram demandas do território. O sistema categoriza e prioriza por parâmetros públicos. Conselheiros sorteados acompanham a execução de forma rastreável.

## Repositórios

- [`mvp-api`](https://github.com/Rede-Civica/mvp-api): back-end NestJS. Monolito modular "O Formigueiro", orientado a eventos.
- [`mvp-web`](https://github.com/Rede-Civica/mvp-web): front-end React, PWA map-first.
- [`docs`](https://github.com/Rede-Civica/docs): modelo conceitual completo e especificações de software.
- [`mvp-docs`](https://github.com/Rede-Civica/mvp-docs): site público de documentação, em [`docs.redecivica.com.br`](https://docs.redecivica.com.br).

## Licença

Todo o código é AGPL-3.0. Copyleft forte para serviços de rede.

O nome e o logo Rede Cívica são marca do projeto. A licença do código não concede direito de uso da marca. A política está em [TRADEMARK.md](https://github.com/Rede-Civica/.github/blob/main/TRADEMARK.md).

## Governança

O processo de desenvolvimento é público. Contribuições seguem o fluxo documentado no `CONTRIBUTING.md` de cada repositório de código e o código de conduta desta org.

No horizonte do projeto, a governança se institucionaliza como fundação sem fins lucrativos, detentora da missão e da marca. O código permanece AGPL-3.0 e o fork permanece possível.

## Como começar

- Modelo conceitual: `rede_civica.md` no repo de docs.
- Contribuição de código: `CONTRIBUTING.md` e `AGENTS.md` nos repos de código.
- Vulnerabilidades: `SECURITY.md` nos repos de código.

### Trilha de aprendizagem do mapa

Para quem quer entender a camada de mapa, do dado ao render, na ordem:

1. Fundamentos: [mapa_e_tiles.md](https://github.com/Rede-Civica/docs/blob/master/mapa_e_tiles.md) no repo `docs`. Conceitos de tile e zoom, formatos de dado e glossário.
2. Geração: [scripts/tiles](https://github.com/Rede-Civica/mvp-api/tree/main/scripts/tiles) no repo `mvp-api`. Como a camada base é gerada a partir do OpenStreetMap, dos prédios da Microsoft, da cobertura vegetal da Overture e do contexto dos vizinhos da América do Sul.
3. Consumo: seção "Mapa — como a camada base funciona" no [README do mvp-web](https://github.com/Rede-Civica/mvp-web#readme). Como o app serve e renderiza os tiles.

## Status

Fase 1 do MVP em desenvolvimento.
