# Diccionario inicial de variables

La notación definitiva se actualizará cuando se incorpore al cuaderno el cambio porcentual del recaudo total.

| Variable del panel | Descripción | Fuente o construcción |
|---|---|---|
| `codigo_departamento` | Código del departamento | DIVIPOLA |
| `departamento` | Nombre del departamento | DIVIPOLA |
| `codigo_municipio` | Código municipal de cinco dígitos | DIVIPOLA |
| `municipio` | Nombre del municipio | DIVIPOLA |
| `año` | Vigencia anual | Construcción del panel |
| `R_ACT_FUT` | Recaudo predial de la vigencia actual | FUT, concepto `TI.A.1.3.1` |
| `R_ANT_FUT` | Recaudo predial de vigencias anteriores | FUT, concepto `TI.A.1.3.2` |
| `R_TOT_FUT` | Recaudo total ajustado a pesos | Suma de `R_ACT_FUT` y `R_ANT_FUT` |
| `R_TOT_CUIPO` | Recaudo total del IPU reportado | CUIPO, concepto `1.1.01.01.200` |
| `R_TOT` | Recaudo total armonizado | FUT en 2012–2020 y CUIPO en 2021–2025 |
| `L_CHIP` | Impuesto predial liquidado o reconocido durante el año | CHIP, cuenta `4.1.05.07` |
| `C_CIERRE_CHIP` | Cartera de predial al cierre del año | CHIP, cuentas por cobrar según catálogo aplicable |
| `C_CHIP` | Cartera disponible al inicio del año | Cartera al cierre del año anterior |
| `y_C` | Cumplimiento predial global observado | `R_TOT / (C_CHIP + L_CHIP)` |
| `y_R` | Reducción neta observada de la cartera | `(C_CHIP - C_CIERRE_CHIP) / C_CHIP` |

Los valores monetarios se expresan en pesos corrientes. Los valores ausentes se mantienen como ausentes en la versión inicial.
