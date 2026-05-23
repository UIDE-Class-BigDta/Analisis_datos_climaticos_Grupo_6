# Análisis de Datos Climáticos con Big Data

Este repositorio contiene el desarrollo del proyecto integrador para la materia de Minería de Datos / Procesamiento de Datos Masivos. El objetivo principal es procesar un gran volumen de información meteorológica histórica para identificar patrones de calentamiento global y predecir anomalías de temperatura utilizando herramientas distribuidas.

## Seccion 1: Tema e integrantes
* **Número de grupo:** 6
* **Tema asignado:** Análisis de datos climáticos
* **Integrantes:**
  * Mateo David Castillo Machero
  * Christian Alexander Salinas Ramon

---

## Seccion 2: Planteamiento del problema
Los ministerios de medio ambiente y los sectores de planificación urbana a nivel global enfrentan un riesgo inminente debido al cambio climático acelerado. Actualmente, las políticas de adaptación y el diseño de infraestructura a largo plazo (como represas, sistemas de alcantarillado o refrigeración urbana) se basan en estimaciones generales que no procesan adecuadamente el histórico masivo de fluctuaciones térmicas de los últimos siglos. 

El Director de Políticas Ambientales necesita un sistema analítico que analice y prediga las tendencias de temperatura y anomalías térmicas futuras con alta precisión. Esto permitirá tomar decisiones estratégicas de mitigación en tiempo real, tales como: reasignar presupuestos para construir infraestructura resiliente al calor extremo, modificar normativas de construcción, o planificar la transición de cultivos agrícolas en zonas vulnerables. Los principales beneficiarios serán los gobiernos locales, que optimizarán sus recursos económicos, y la población civil, que sufrirá un menor impacto ante fenómenos climáticos extremos.

---

## Seccion 3: Dataset seleccionado
Para garantizar un procesamiento eficiente y evitar la saturación de memoria en entornos de ejecución, se trabaja con la versión agregada a nivel de país del proyecto Berkeley Earth:

* **Nombre del dataset:** Climate Change: Earth Surface Temperature Data (Berkeley Earth - By Country)
* **URL de descarga:** https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data
* **Archivo utilizado:** GlobalLandTemperaturesByCountry.csv
* **Volumen:** 577,462 filas y 4 columnas.
* **Variable principal de análisis:** AverageTemperature (Variable objetivo continua para la predicción de tendencias climáticas).
* **Formato del archivo:** CSV.

---

## Seccion 4: Objetivo general
Desarrollar un sistema de análisis y predicción de calentamiento global utilizando procesamiento distribuido con Spark y modelos de Machine Learning con Spark MLlib, capaz de procesar cientos de miles de registros históricos para predecir la variable AverageTemperature minimizando el margen de error, facilitando así la toma de decisiones preventivas en infraestructura y políticas públicas a los tomadores de decisiones gubernamentales.

---

## Seccion 5: Tres objetivos específicos
1. **Analizar** el dataset climático global mediante un Exploratory Data Analysis (EDA) para identificar tendencias seculares, tratar la estacionalidad de los datos y perfilar los países con mayor varianza térmica histórica.
2. **Implementar** un pipeline ETL con PySpark que filtre los registros históricos con alto porcentaje de nulos, impute valores faltantes modernos y exporte el dataset limpio en formato Parquet para optimizar la lectura distribuida.
3. **Construir y evaluar** modelos predictivos (como Random Forest Regressor) utilizando Spark MLlib, comparando su rendimiento mediante métricas de validación como RMSE (Root Mean Squared Error) y R².

---

## Tecnologías Utilizadas
* **Lenguaje principal:** Python 3
* **Procesamiento Big Data:** Apache Spark & PySpark (DataFrames & SQL)
* **Machine Learning:** Spark MLlib
* **Entorno de ejecución:** Google Colab
* **Control de versiones:** GitHub
