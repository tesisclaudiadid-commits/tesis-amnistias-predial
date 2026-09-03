# Datos del proyecto

Las bases no se almacenan en GitHub. El cuaderno espera la carpeta raíz:

`/content/drive/MyDrive/Datos`

Estructura actual en Google Drive:

```text
Datos/
├── originales/
│   ├── chip/
│   ├── municipios/
│   ├── oec/
│   └── predial/
└── panel/
    ├── ConstruccionPanel.ipynb
    └── Panel_Inicial_2007_2025.xlsx
```

Los archivos de `originales/` deben conservarse sin modificaciones. Los productos generados por el código se guardan en `panel/`.

## Fuentes principales

- CHIP, Contaduría General de la Nación: saldos contables del Impuesto Predial Unificado.
- FUT, 2012–2020: ejecución de ingresos.
- CUIPO, 2021–2025: ejecución de ingresos.
- DIVIPOLA: identificación de municipios.

Los nombres exactos de archivos, cuentas, conceptos y reglas de validación se documentarán en `documentacion/`.
