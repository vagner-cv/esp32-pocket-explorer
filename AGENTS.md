# AGENTS.md — contexto de desenvolvimento para Codex

Projeto: **Pocket Explorer**, um gadget portátil com ESP32-S3, tela de 240×240 e sensores externos.

## Tarefa principal
Continuar o firmware original do usuário; **não reinventar o projeto do zero**. Código-fonte da última versão ainda não foi importado.

## Hardware e GPIOs registrados
Leia `docs/HARDWARE.md` primeiro. Resumo:
- Placa Waveshare **ESP32-S3-LCD-1.3**, LCD ST7789 240×240, 16 MB Flash, 8 MB PSRAM.
- Display interno: DC38 CS39 SCK40 MOSI41 RST42 BL20.
- IMU QMI8658 interna: SDA47/SCL48.
- GPS TX → RX ESP32 em **GPIO1**.
- I²C **externo** GPIO8 (SDA), GPIO9 (SCL): BME280 e QMC5883L.
- Botões no protótipo: **GPIO10/11/12** (funções anterior/OK/próximo).
- Leitor microSD interno, cartão de 32 GB usado.
- Bateria 3,7 V 500 mAh **não assumir conectada** (conector incompatível relatado).
- Confirmar tudo contra o .ino físico; sinalizar incertezas em vez de inventar.

## Telas e experiência
Menu, álbum de fotos, ambiente local, previsão do tempo, mapas/GPS, bússola, relógio e ajustes. Exemplos visuais ilustrativos em `docs/images/`; **não são screenshots de firmware validado**.
Temas discutidos: Natureza, Cyberpunk, Pip-Boy e Matrix.

## Práticas
1. Preservar funcionalidades do firmware existente e fontes de imagem/código ao importar.
2. Evitar incompatibilidades entre as diferentes variantes Waveshare.
3. Não introduzir dependências de hardware não existente sem explicitar.
4. Não gravar credenciais Wi-Fi, chaves de API ou tokens no repositório público.
5. Ao propor alterações, explicar impactos de memória, consumo e performance.
6. Incluir orientação de testes concretos e distinguir teste realizado de plano.
7. Documentar GPIOs, sensores e bibliotecas utilizados pelo firmware real.
8. Se dados adicionais forem necessários, solicitar ao usuário o ZIP da **versão real mais recente**.
9. Componentes visuais da pasta `docs/images/` são esquemas/maquetes ilustrativas, não comprovação de recurso.
