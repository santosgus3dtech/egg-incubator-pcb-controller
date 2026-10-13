# Egg Incubator PCB Controller

[English / README principal](README.md) · Português (Brasil)

Estudo de caso de hardware para um controlador de chocadeira com Arduino UNO R4 WiFi,
com revisões de esquemático no EasyEDA, conversão de 12 V para 5 V por meio de um
regulador buck AP63205, RTC, encoder, sensores, saída de relé e pontos de teste.

![Fluxo do hardware](docs/images/hardware-flow.svg)

## O que está neste repositório público

- Revisão 3.7 do EasyEDA em formato JSON.
- Lista de materiais (BOM) preliminar da revisão 3.7.
- Notas técnicas do regulador buck AP63205 e das proteções de entrada.
- Capturas PNG do esquemático para revisão rápida.
- Pacotes de importação do EasyEDA exportados em `releases/`.

Backups locais, dados da aplicação, histórico bruto e caches foram deixados de fora intencionalmente.

## Destaques técnicos

- Entrada de 12 V protegida com fusível, MOSFET de canal P e TVS.
- Regulação de 5 V com AP63205, um indutor de 4.7 uH e capacitores especificados.
- Jumpers para isolar a alimentação do Arduino, a alimentação dos relés e os pull-ups de I2C.
- RTC DS3231 para controle por etapas e recuperação após perda de energia.
- Encoder rotativo, buzzer ativo, sensor de nível e sensor ambiental I2C opcional.
- Lista de verificação de layout para manter sinais sensíveis longe do nó de comutação do regulador buck.

## Estrutura

```text
easyeda/             # JSONs EasyEDA e BOM
docs/                # notas tecnicas e screenshots
releases/            # pacotes de importacao EasyEDA
```

## Imagens

![Controle](docs/screenshots/chocadeira_rev_3_7_uno_r4_wifi_ap63205_buck_sheet_1_rev_3.7_esquematico_controle.png)

![Buck AP63205](docs/screenshots/chocadeira_rev_3_7_uno_r4_wifi_ap63205_buck_sheet_3_rev_3.7_buck_ap63205_12v_5v.png)

## Portfólio

Este é um projeto útil de portfólio público porque demonstra leitura de datasheets,
tomada de decisões de hardware, organização de BOM, revisões técnicas, verificações
do repositório e entregáveis prontos para fabricação. Consulte
[docs/portfolio-case-study.md](docs/portfolio-case-study.md).
