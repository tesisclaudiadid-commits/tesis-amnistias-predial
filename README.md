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

Ya se dispone de los datos recopilados y depurados de recaudo, liquidación y cartera. El cuaderno contiene el procesamiento de FUT, CUIPO y CHIP y el código actualizado de las cuatro variables. La actualización del bloque de variables pasó pruebas con datos de ejemplo: fórmulas, signos, ausentes, ceros, años no consecutivos, duplicados y reejecución. Falta ejecutar esta versión con los originales en Drive y revisar los resultados reales.

Pendientes: construir D_it, seleccionar covariables, evaluar supuestos y estimar efectos. Las variables observadas no son estimaciones de impacto.

## Estructura

- `notebooks/`: cuaderno para Colab, sin salidas guardadas.
- `documentacion/`: fuentes y diccionario de variables.
- `datos/`: instrucciones; los originales y el panel permanecen en Drive.

## Convenciones

Resultados en proporciones. No se imputan ausentes ni se recortan extremos. y_car es variación de cartera: negativo significa disminución, positivo significa aumento. Sustituye la antigua y_R con signo contrario. El crecimiento de 2012 requiere recaudo de 2011 y queda ausente con la cobertura actual.
