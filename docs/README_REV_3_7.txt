Chocadeira rev 3.7 - EasyEDA

Arquivo para importar:
1-Schematic_chocadeira_rev_3_7_uno_r4_wifi_ap63205_buck.json

O que mudou:
- Mantem a base da rev 3.6 com encoder, RTC DS3231, nivel de agua, controle por fases e buck AP63205.
- Remove a alimentacao por modulo LM2596.
- Adiciona jumpers JP_ARD_5V, JP_RELE_5V e JP_I2C_PU para testes e isolamento.
- Adiciona J_BUZZ1 para modulo buzzer ativo 5 V no pino D4.
- Adiciona J_ENV1 para sensor I2C melhor opcional, como SHT31/SHT35/HDC302x.
- RTC DS3231 ja estava no projeto; agora esta marcado como modulo com bateria CR2032.
- Arduino passa a ser alimentado pelo pino 5V regulado via JP_ARD_5V; VIN fica sem uso.
- Atualiza lista de footprints/candidatos compraveis no checklist e BOM.
- Inclui lista tecnica no arquivo POWER_BUCK_AP63205_DESIGN_NOTES.txt.
- Inclui BOM preliminar no arquivo BOM_REV_3_7_AP63205.csv.

Abra pelo EasyEDA em File > Open > EasyEDA... > Import File.