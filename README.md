# Dow Jones Index — Análisis Exploratorio de Datos (EDA)

![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=flat&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-white?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter)

Análisis exploratorio de las 30 acciones que componían el **Dow Jones Industrial Average** durante el primer y segundo trimestre de 2011. 

El objetivo principal de este proyecto es aplicar técnicas de manipulación de datos, análisis estadístico y visualización con Python, trabajando sobre un dataset financiero real para extraer insights de mercado.

## Dataset

* **Fuente:** [UCI Machine Learning Repository — Dow Jones Index](https://archive.ics.uci.edu/ml/datasets/Dow+Jones+Index)
* **Descripción:** El dataset contiene registros semanales del precio de cierre, apertura, máximos, mínimos y volumen de 30 empresas listadas en el Dow Jones durante 2011. 
* El archivo original (`dow_jones_index.data`) se encuentra en la carpeta `data/` del repositorio.

## Estructura del Proyecto

```text
dow-jones-eda/
├── Data/
│   └── dow_jones_index.data
├── ProyectoFinal.ipynb
├── requirements.txt
├── .gitignore
└── README.md

## Contenido del análisis

**1. Carga y limpieza de datos**
- Selección y renombre de columnas relevantes
- Parseo de fechas con `pd.to_datetime`
- Conversión de precios desde formato string (`$16.42`) a float

**2. Distribución temporal**
- Distribución de registros por año y mes
- Explicación del desbalance observado en abril respecto al resto de los meses

**3. Estadísticas descriptivas por acción**
- Precio de cierre promedio por empresa
- Desviación estándar como medida de volatilidad
- Identificación de las acciones más y menos volátiles

**4. Análisis de correlación**
- Reestructuración del DataFrame con `pivot_table` para comparación entre acciones
- Correlación de Pearson entre CAT (la acción más volátil) y el resto
- Visualización de las correlaciones más altas y más bajas

---

## Principales conclusiones

- IBM tuvo el precio de cierre promedio más alto (163,10 USD), mientras que BAC tuvo el más bajo (13,05 USD).
- CAT fue la acción más volátil con una desviación estándar de 6,22 USD; AA fue la menos volátil con 0,77 USD.
- Ninguna acción presentó una correlación negativa significativa con CAT durante el período analizado.

---

## Tecnologías utilizadas

- Python 3.13
- pandas
- NumPy
- Matplotlib

---

## Cómo ejecutar el proyecto

1. Clonar el repositorio y navegar a la carpeta del proyecto.
2. Instalar las dependencias:

```bash
pip install -r requirements.txt
```

3. Abrir el notebook:

```bash
jupyter notebook ProyectoFinal.ipynb
```
