# Estado atual do controlador de chocadeira

Revisão: 13/10/2026. Git inicial limpo. Etapa comprovada: leitura das notas técnicas e inventário dos artefatos. Nenhuma aplicação EasyEDA, importação, simulação, fabricação ou teste elétrico foi executado.

## Arquitetura documentada e observação

[README](../README.md) e [notas rev 3.7](README_REV_3_7.txt) descrevem entrada 12 V protegida, conversão AP63205 para 5 V, UNO R4 WiFi, DS3231 com bateria, encoder, nível de água, buzzer, relé e sensor I2C opcional. As [notas do buck](POWER_BUCK_AP63205_DESIGN_NOTES_REV_3_7.txt) mantêm os componentes candidatos e orientações de layout; não se repetem suas estimativas térmicas como resultados físicos.

O [JSON de esquema](../easyeda/1-Schematic_chocadeira_rev_3_7_uno_r4_wifi_ap63205_buck.json) foi identificado como pacote com chaves `editorVersion`, `docType`, `schematics` e metadados. `easyeda/` também contém PCB nomeado rev 3.3, BOM rev 3.7 e outros JSONs; a correspondência do PCB antigo ao esquema rev 3.7 não foi validada. Pacotes ZIP em `releases/` existem, sem abertura nativa nesta revisão.

## Regras e pendências existentes

A fonte [README_REV_3_7](README_REV_3_7.txt) registra remoção do módulo LM2596, jumpers de isolamento de alimentação/I2C, alimentação regulada no pino 5V e VIN sem uso. Isso é descrição da revisão, não ensaio do circuito. Não se inventou motivo histórico adicional.

As [notas técnicas](POWER_BUCK_AP63205_DESIGN_NOTES_REV_3_7.txt) deixam pendentes footprints conforme peças/montagem, layout manual da área buck, backfeed USB/5V, dimensionamento de proteção conforme cargas e Footprints Verification/Convert to PCB/DRC/ERC/revisão antes de Gerber. A existência de releases não comprova fabricação pronta ou aprovação elétrica.

## Operação e plano

A instrução de importação existente é EasyEDA `File > Open > EasyEDA... > Import File`. Não foi identificado firmware ou comando CLI de build/teste. Importação e todas as verificações nativas: **não executado nesta tarefa**.

Não há aprovação de fabricação identificada. Próximos passos documentados a confirmar: (1) reconciliar revisões PCB/esquema e footprints; (2) revisar layout/proteções/USB com componentes reais; (3) executar o checklist nativo antes de gerar/fabricar. O [estudo de caso](portfolio-case-study.md) é apresentação, sem certificação de hardware.

[Índice](INDEX.md).
