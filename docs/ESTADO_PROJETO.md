# Estado atual e roteiro de migração

## O que já foi desenvolvido/discutido

- Tela principal/menu com várias opções por página e títulos menores.
- Navegação por **3 botões** (anterior, OK e próximo).
- Telas: **Álbum**, **Ambiente local**, **Tempo na cidade**, **Explorar (mapa/GPS)**, **Bússola**, **Relógio** e **Ajustes**.
- Temas experimentais: **Natureza**, **Cyberpunk**, **Pip-Boy** e protótipo **Matrix**.
- GPS externo enviando NMEA; em testes posteriores foi relatada **posição válida**, com mapa exibido.
- Mapa local com blocos em cache no microSD, atualização da orientação, três níveis de zoom.
- Previsão do tempo com estado atual e próximos dias, ícones de sol/nuvem/chuva e mínimas/máximas.
- Leitura local de temperatura, umidade e pressão via módulo ambiental.
- Bússola usando magnetômetro.
- Álbum com imagens na memória/cartão; usuário pode escolher uma ou mais.
- Duração de telas: ciclo citado de **15 s** para informações e imagem e **30 s** para mapa, sujeito ao sketch final.
- Planejamento de energia portátil com Li-ion 3,7 V; conexão da bateria ainda pendente.

## Situação da importação de código

O código-fonte da versão mais recente **não está presente neste repositório**. Foram mencionados arquivos como `pocket-explorer-v0.37-bateria-zoom.zip`, além de revisões posteriores até v0.39, mas o arquivo original atual ainda precisa ser fornecido.

**Não gerar um firmware substituto só com base nesta documentação**. O próximo passo é importar o ZIP ou `.ino` exato da instalação funcional mais recente.

## Etapas para Codex

1. Ler `README.md`, `docs/HARDWARE.md`, `AGENTS.md` e as imagens de referência.
2. Importar o firmware original sem refatoração inicial; preservar imagens, mapas e demais assets.
3. Identificar configuração de build, dependências e pinagem realmente usada.
4. Atualizar `docs/HARDWARE.md` com dados confirmados e avisos sobre alternativas.
5. Compilar com as bibliotecas/versões registradas. Não alegar teste de hardware sem executar.
6. Abrir pequenas alterações por etapa (não reorganizar o projeto inteiro na primeira edição).
