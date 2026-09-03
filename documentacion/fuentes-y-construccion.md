# Fuentes y construcción del panel

Este documento resume la implementación que contiene actualmente `notebooks/ConstruccionPanel.ipynb`. No sustituye las fuentes oficiales ni el registro posterior de decisiones metodológicas.

## Inventario actual

| Componente | Periodo | Archivo o patrón | Extracción principal |
|---|---:|---|---|
| Municipios | 2007–2025 | `DIVIPOLA_Municipios.xlsx` | Códigos y nombres para formar el panel municipio-año |
| FUT | 2012–2020 | `2012_FutIngresos.xlsx`; luego `{año}_FUTIngresos.xlsx` | `TI.A.1.3.1` vigencia actual y `TI.A.1.3.2` vigencias anteriores |
| CHIP | Cierres 2007–2025 | `CHIP_CGN_2007_2026T2_EntGob_130507_131007_410507.xls` | Cuentas `1.3.05.07`, `1.3.10.07` y `4.1.05.07` |
| CUIPO | 2021–2025 | `{año}_8_CUIPOB_EJECUCION_DE_INGRESOS.xlsx`; 2025 en `.xlsb` | Concepto `1.1.01.01.200`, campo `Total Recaudo` |

## Reglas implementadas

- Los valores FUT de 2012–2016 se multiplican por 1.000; los de 2017–2020 ya están expresados en pesos.
- `R_TOT_FUT` es la suma de `R_ACT_FUT` y `R_ANT_FUT` cuando ambos componentes están disponibles.
- `R_TOT` toma `R_TOT_FUT` en 2012–2020 y `R_TOT_CUIPO` en 2021–2025.
- `L_CHIP` corresponde al saldo final anual de la cuenta `4.1.05.07`.
- `C_CIERRE_CHIP` suma las cuentas `1.3.05.07` y `1.3.10.07` hasta 2017; desde 2018 utiliza `1.3.05.07`.
- `C_CHIP` para el año (t) es `C_CIERRE_CHIP` del año (t-1).
- La versión actual no imputa ausentes, no reemplaza ausentes por cero y no elimina valores extremos.

## Variables de resultado presentes en el cuaderno

- `y_C = R_TOT / (C_CHIP + L_CHIP)`: cumplimiento predial global observado.
- `y_R = (C_CHIP - C_CIERRE_CHIP) / C_CHIP`: reducción neta observada de la cartera.

La metodología vigente también contempla el cambio porcentual del recaudo total. Su incorporación al código y la actualización de la notación se harán en una versión posterior.
