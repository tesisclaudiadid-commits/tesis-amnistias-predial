# Amnistías tributarias e impuesto predial municipal

Repositorio de la tesis de Claudia Yineth Pineda Cortina.

## Alcance

- Unidad: municipio-año; periodo principal 2012–2025.
- Fuentes: CHIP y FUT/CUIPO mediante CIFFIT.
- Cuatro variables de interés: cumplimiento global, deuda relativa, crecimiento del recaudo y variación de cartera.

## Ejecución

[Abrir el cuaderno en Google Colab](https://colab.research.google.com/github/tesisclaudiadid-commits/tesis-amnistias-predial/blob/main/notebooks/ConstruccionPanel.ipynb).

Montar Drive y ubicar los archivos originales en `MyDrive/Datos`, según `documentacion/fuentes-y-construccion.md` y `datos/README.md`. Ejecutar las celdas en orden. El cuaderno exporta el panel a Drive.

## Estado del trabajo

Ya se dispone de los datos recopilados y depurados de recaudo, liquidación y cartera. El cuaderno contiene el procesamiento de FUT, CUIPO y CHIP y el código actualizado de las cuatro variables. La actualización del bloque de variables pasó pruebas con datos de ejemplo: fórmulas, signos, ausentes, ceros, años no consecutivos, duplicados y reejecución. El panel exportado desde Drive el 29 de octubre de 2026 contiene 20.957 filas y 18 columnas. Se verificaron la unicidad municipio-año y las fórmulas de las cuatro variables en todas sus filas; esta comprobación no sustituye la revisión de las fuentes originales.

Pendientes: construir D_it, seleccionar covariables, evaluar supuestos y estimar efectos. Las variables observadas no son estimaciones de impacto.

## Estructura

- `notebooks/`: cuaderno para Colab, sin salidas guardadas.
- `documentacion/`: fuentes y diccionario de variables.
- `datos/`: instrucciones y panel inicial descargable; los archivos originales permanecen en Drive.

## Convenciones

Resultados en proporciones. No se imputan ausentes ni se recortan extremos. y_car es variación de cartera: negativo significa disminución, positivo significa aumento. Sustituye la antigua y_R con signo contrario. El crecimiento de 2012 requiere recaudo de 2011 y queda ausente con la cobertura actual.

## Panel inicial disponible

[Descargar Panel_Inicial_2007_2025.xlsx](datos/panel/Panel_Inicial_2007_2025.xlsx?raw=true)

Incluye 1.103 municipios, años 2007–2025, 20.957 filas y 18 columnas, entre ellas `y_cum`, `y_deu`, `y_rec` y `y_car`. El periodo principal del estudio sigue siendo 2012–2025. La disponibilidad varía por variable y año; los datos ausentes no se rellenaron. El tratamiento D_it y las covariables aún no están incorporados. Para consultar o analizar el panel publicado no hace falta acceso a Drive; para reconstruirlo desde las fuentes se necesitan los originales y las rutas del cuaderno.
