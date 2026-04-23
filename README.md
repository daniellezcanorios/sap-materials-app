# Procesador de Materiales para Inventarios Físicos SAP S4/HANA Almacenes EPM

Aplicación web en **Streamlit** que permite subir el archivo de materiales exportado desde SAP y obtener:

- Tablas interactivas con agrupaciones:
  - Stock regular (Centro–Almacén) para identificar material de inventario a ejecutar mediante transacción MI31
  - Stock de proyectos (Imputación Q con Elemento PEP (Centro–Almacén–Elemento PEP) para identificar material de inventario a ejecutar mediante transacción MI01 de Stock Especial Individual
- Exportación a Excel con una hoja por cada **Elemento PEP**, mostrando columnas **Material** y **Lote**, ordenadas por **Ubicación** y luego por **Material**. Para facilitar creación de documento de inventario físico para material de proyectos y evitar errores o dejar materiales por fuera o en un documento que no corresponde.

## 🚀 Cómo usar

1. Abre la aplicación en Streamlit Cloud:  
   👉 [Enlace de la app](https://sap-materials-daniellezcanorios-app-gjzvae39blbpetykempkph.streamlit.app/)

2. Sube tu archivo exportado de SAP mediante transacción Stock varios materiales (`.xlsx`).

3. Visualiza las tablas directamente en la página.

4. Descarga el archivo Excel procesado con un clic.

## 🛠️ Requisitos

- Python 3.9+
- Librerías: `streamlit`, `pandas`, `openpyxl`

Instalación local:
```bash
pip install -r requirements.txt
streamlit run app.py
