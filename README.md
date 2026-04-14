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
* El archivo original (`dow_jones_index.data`) se encuentra en la carpeta `Data/` del repositorio.

## Estructura del Proyecto

```text
Proyecto-Final-Python/
├── Data/
│   └── dow_jones_index.data
├── ProyectoFinal.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Contenido del Análisis

El desarrollo en el notebook abarca las siguientes etapas:

1. **Carga y Limpieza de Datos:**
   * Selección y renombramiento de columnas relevantes.
   * Parseo de fechas utilizando `pd.to_datetime`.
   * Conversión de precios desde formato string (ej. `$16.42`) a `float` numérico mediante funciones Lambda.
2. **Distribución Temporal:**
   * Análisis de la distribución de registros por año y mes.
   * Identificación y explicación de desbalances temporales (ej. anomalía de registros en el mes de abril).
3. **Estadísticas Descriptivas por Acción:**
   * Cálculo del precio de cierre promedio por empresa.
   * Uso de la **desviación estándar ($\sigma$)** como medida fundamental de volatilidad y riesgo.
   * Ranking de las acciones más y menos volátiles del mercado.
4. **Análisis de Correlación:**
   * Reestructuración del DataFrame utilizando `pivot_table` para alinear series temporales.
   * Cálculo de la Correlación de Pearson entre la acción más volátil (CAT) y el resto del mercado.
   * Visualización gráfica de las correlaciones más fuertes y débiles.

## Principales Conclusiones

* **Precios:** **IBM** registró el precio de cierre promedio más alto (**163.10 USD**), mientras que **BAC** cotizó al valor más bajo (**13.05 USD**).
* **Volatilidad:** **CAT** (Caterpillar) se posicionó como la acción más volátil e impredecible del período analizado con una desviación estándar de **6.22 USD**. En contraparte, **AA** (Alcoa) fue la más estable (**0.77 USD**).
* **Correlación:** Durante el primer semestre de 2011, ninguna acción del índice presentó una correlación negativa significativa respecto a CAT, indicando un movimiento de mercado fuertemente acoplado.

## Cómo ejecutar el proyecto localmente

1. Clonar este repositorio:
   ```bash
   git clone [https://github.com/TomasBulacio/Proyecto-Final-Python.git](https://github.com/TomasBulacio/Proyecto-Final-Python.git)
   ```
2. Navegar a la carpeta del proyecto:
   ```bash
   cd Proyecto-Final-Python
   ```
3. Instalar las dependencias requeridas:
   ```bash
   pip install -r requirements.txt
   ```
4. Abrir el entorno de desarrollo:
   ```bash
   jupyter notebook ProyectoFinal.ipynb
   ```
