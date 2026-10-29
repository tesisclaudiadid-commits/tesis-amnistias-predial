# Diccionario de variables

Notación alineada con las cuatro variables de interés del proyecto. Las razones se almacenan en proporciones, sin multiplicar por 100.

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
| `y_cum` | Cumplimiento global | `R_TOT / (C_CHIP + L_CHIP)` |
| `y_deu` | Deuda relativa | `C_CIERRE_CHIP / L_CHIP` |
| `R_TOT_PREVIO` | Recaudo del año calendario anterior | Unión por municipio y año anterior; no salta años ausentes |
| `y_rec` | Crecimiento del recaudo | `(R_TOT - R_TOT_PREVIO) / R_TOT_PREVIO` |
| `y_car` | Variación de cartera | `(C_CIERRE_CHIP - C_CHIP) / C_CHIP` |

Los valores monetarios se expresan en pesos corrientes. Los valores ausentes se mantienen como ausentes en la versión inicial.

Los denominadores deben ser positivos. No se imputan ausentes ni se recortan extremos. Se señalan componentes negativos y cumplimiento mayor que uno para revisión. `y_car` sustituye la antigua reducción de cartera `y_R`: tiene signo contrario. El crecimiento de 2012 queda ausente porque el recaudo disponible empieza en 2012. Las carteras de cierre provienen del cierre contable observado de cada año, incluido 2025; no se necesita un archivo separado de 2026 para ese cierre.

La variable D_it, las covariables y las estimaciones causales quedan pendientes. El panel exportado desde Drive el 29 de octubre de 2026 está publicado en `datos/panel/Panel_Inicial_2007_2025.xlsx`. Se verificaron las cuatro fórmulas en sus 20.957 filas y la unicidad municipio-año.
