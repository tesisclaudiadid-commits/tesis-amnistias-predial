# Datos del proyecto

## Panel inicial publicado

[Panel_Inicial_2007_2025.xlsx](panel/Panel_Inicial_2007_2025.xlsx?raw=true)

Copia del Excel exportado en Google Drive el 29 de octubre de 2026, sin modificar su contenido. Incluye 20.957 filas, 18 columnas y 1.103 municipios durante 2007–2025. El periodo principal de investigación es 2012–2025.

Las cuatro variables son `y_cum`, `y_deu`, `y_rec` y `y_car`. Véase el diccionario en `documentacion/diccionario-variables.md`.

Se verificaron las cuatro fórmulas fila a fila y la ausencia de duplicados municipio-año. No se imputaron datos. Los recuentos disponibles en todo el panel son:

| Variable | Observaciones disponibles |
|---|---:|
| y_cum | 13.180 |
| y_deu | 19.953 |
| y_rec | 11.913 |
| y_car | 17.804 |

Estas cantidades incluyen años anteriores a 2012 cuando hay información. No significan que todas las variables estén disponibles para todos los municipios y años. La base es inicial: no contiene D_it, covariables ni estimaciones de impacto.

SHA-256 del Excel: `ca1fbc1f24858a9aa5c1f117b42b27dbf398221d971348b4ccf2d4d560b069ce`.

## Reproducción desde los originales

El cuaderno espera la carpeta raíz `/content/drive/MyDrive/Datos`, con las carpetas `originales/chip/`, `originales/municipios/` y `originales/predial/`. Los originales se conservan en Drive; no están incluidos en GitHub. El cuaderno exporta el panel a `Datos/panel/`.

Fuentes: CHIP (Contaduría General de la Nación), FUT 2012–2020 y CUIPO 2021–2025 mediante CIFFIT, y DIVIPOLA. Los archivos, cuentas y reglas de procesamiento se describen en `documentacion/fuentes-y-construccion.md`.
