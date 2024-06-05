# Análisis de Siniestros Viales en la Ciudad de Buenos Aires (2016-2021)

## Índice
- [Introducción](#introducción)
- [Fuente de Datos](#fuente-de-datos)
- [Metodología](#metodología)
  - [Extracción, Transformación y Carga (ETL)](#extracción-transformación-y-carga-etl)
  - [Análisis Exploratorio de Datos (EDA)](#análisis-exploratorio-de-datos-eda)
  - [Definición y Seguimiento de KPIs](#definición-y-seguimiento-de-kpis)
  - [Desarrollo de Dashboard](#desarrollo-de-dashboard)
- [Resultados y Conclusiones](#resultados-y-conclusiones)
  - [KPI 1 - Tasa de homicidios en siniestros viales](#kpi-1---tasa-de-homicidios-en-siniestros-viales)
  - [KPI 2 - Accidentes mortales de motociclistas](#kpi-2---accidentes-mortales-de-motociclistas)
  - [KPI 3 - Proporción de víctimas fatales por tipo de vehículo](#kpi-3---proporción-de-víctimas-fatales-por-tipo-de-vehículo)
- [Repositorio de GitHub](#repositorio-de-github)
- [Autor](#autor)

## Introducción

Este proyecto tiene como objetivo analizar los datos de homicidios en siniestros viales ocurridos en la Ciudad Autónoma de Buenos Aires durante el periodo 2016-2021. El propósito es generar información relevante que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en accidentes de tránsito.

El trabajo ha sido encomendado por el Observatorio de Movilidad y Seguridad Vial (OMSV), un centro de estudios dependiente de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires.

## Fuente de Datos

Los datos utilizados en este análisis provienen de las siguientes fuentes:

- **Buenos Aires Data**: Se nos proporcionó un dataset en formato xlsx con información sobre homicidios en siniestros viales en la Ciudad de Buenos Aires durante el periodo 2016-2021. El archivo se encuentra en la carpeta [`Data`](./Data).

- **Diccionario de Datos**: Junto con el dataset, se incluyen dos hojas adicionales que sirven como diccionario de datos para facilitar la comprensión de la información contenida en las hojas principales. Estos diccionarios se encuentran en la carpeta [`Data`](./Data).

## Metodología

Para llevar a cabo este proyecto, se siguieron los siguientes pasos:

### Extracción, Transformación y Carga (ETL)
Se realizó un proceso de ETL para preparar los datos antes del análisis. Esto incluyó la extracción de los datos desde las fuentes originales, la limpieza y transformación de los mismos para garantizar su calidad y consistencia, y finalmente, la carga de los datos procesados en una base de datos para su posterior uso. El proceso de ETL se encuentra detallado en el archivo [`ETL.ipynb`](./notebooks/ETL.ipynb).

### Análisis Exploratorio de Datos (EDA)
Se realizó un análisis exhaustivo de los datos utilizando Python y las librerías pandas, numpy y matplotlib en un notebook de Jupyter. Durante este proceso, se llevaron a cabo las siguientes tareas:
- Búsqueda y tratamiento de valores faltantes, atípicos y duplicados.
- Análisis de la distribución de las variables y su relación con los siniestros viales.
- Generación de visualizaciones coherentes para una mejor comprensión de los datos.
- Documentación detallada de los hallazgos y conclusiones en cada etapa del análisis.

El análisis exploratorio de datos se encuentra en el archivo [`EDA.ipynb`](./notebooks/EDA.ipynb).

### Definición y Seguimiento de KPIs
Antes de desarrollar el dashboard, se establecieron tres Key Performance Indicators (KPIs) para medir el progreso en la reducción de víctimas fatales en siniestros viales:
- KPI 1: Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en comparación con el semestre anterior. El archivo relacionado a este KPI se encuentra en [`kpi1.csv`](./assets/kpi1.csv).
- KPI 2: Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, respecto al año anterior. El archivo relacionado a este KPI se encuentra en [`kpi2.csv`](./assets/kpi2.csv).
- KPI 3 (propuesto por el equipo): Disminuir en un 5% la proporción de víctimas fatales menores de 25 años en el próximo trimestre, en comparación con el trimestre actual. El archivo relacionado a este KPI se encuentra en [`kpi3.csv`](./assets/kpi3.csv).

### Desarrollo de Dashboard
Se creó un dashboard interactivo utilizando la herramienta Power BI para presentar los principales insights de forma clara y accesible. Los KPIs definidos anteriormente se implementaron en el dashboard para su seguimiento. Además, el dashboard incluye:
- Filtros para explorar los datos según diferentes criterios (fecha, tipo de siniestro, características de las víctimas, etc.).
- Gráficos y visualizaciones que facilitan la interpretación de la información.
- Un diseño intuitivo y estéticamente agradable para mejorar la experiencia del usuario.

El archivo del dashboard se encuentra en la carpeta [`Dashboard`](./Dashboard/Dashboard.pbix).

## Resultados y Conclusiones

A través del análisis exploratorio de datos, la definición de KPIs y la visualización en el dashboard, se obtuvieron los siguientes resultados clave en relación a los siniestros viales de la Ciudad de Buenos Aires durante el periodo 2016-2021:

### KPI 1 - Tasa de homicidios en siniestros viales
- En el último semestre, la tasa de homicidios en siniestros viales fue de 1.37 por cada 100,000 habitantes.
- Esto representa una reducción del 21.15% en comparación con el semestre anterior, donde la tasa fue de 1.73 por cada 100,000 habitantes.
- Se logró superar la meta de reducción del 10% establecida para este KPI.

### KPI 2 - Accidentes mortales de motociclistas
- En el año 2021, se registraron 46 accidentes mortales de motociclistas.
- Esto representa un aumento del 70.37% respecto al año 2020, donde se registraron 27 accidentes mortales de motociclistas.
- No se logró alcanzar la meta de reducción del 7% establecida para este KPI, que habría significado tener 25 o menos accidentes mortales de motociclistas en 2021.

### KPI 3 - Proporción de víctimas fatales por tipo de vehículo
- Las motocicletas representan el 43.00% de las víctimas fatales en siniestros viales.
- Los peatones representan el 38.34% de las víctimas fatales.
- Los automóviles representan el 12.10% de las víctimas fatales.
- Otros tipos de vehículos (bicicletas, vehículos de carga, transporte de pasajeros, etc.) representan proporciones menores de víctimas fatales.

Además de estos resultados específicos de los KPIs, se identificaron los siguientes patrones y tendencias clave:

- La mayoría de las víctimas fatales son hombres jóvenes entre 20 y 35 años.
- Se observa una concentración de accidentes fatales en ciertas zonas geográficas de la ciudad.
- Los fines de semana y los horarios nocturnos presentan una mayor incidencia de siniestros con víctimas fatales.

Basándonos en estos insights, se recomienda a las autoridades considerar las siguientes medidas para reducir las muertes por siniestros viales:

1. Implementar campañas de concientización y educación vial dirigidas especialmente a hombres jóvenes y motociclistas.
2. Reforzar los controles y la seguridad vial en las zonas identificadas como de alto riesgo.
3. Promover el uso de equipos de protección adecuados para motociclistas y ciclistas.
4. Aumentar la presencia policial y los controles de alcoholemia durante los fines de semana y en horarios nocturnos.
5. Mejorar la infraestructura vial en puntos críticos para reducir la peligrosidad de ciertos tramos, especialmente para peatones y motociclistas.

## Repositorio de GitHub

El presente repositorio contiene los siguientes archivos y carpetas:

- [`Data`](./Data/): Carpeta con los archivos de datos originales proporcionados por el OMSV.
- [`CleanData`](./CleanData/): Carpeta con los datos limpios y procesados.
- [`ETL.ipynb`](./notebooks/ETL.ipynb): Archivo ETL.
- [`EDA.ipynb`](./notebooks/EDA.ipynb): Archivo EDA.
- [`Dashboard`](./Dashboard/): Carpeta con los archivos relacionados al dashboard desarrollado en Power BI.
- [`assets`](./assets/): Carpeta con imágenes y gráficos generados durante el análisis.
- [`README.md`](./README.md): Este archivo, que proporciona una descripción general del proyecto y sus resultados.

## Autor

Este proyecto fue desarrollado por Sebastian Quintero como parte de una iniciativa del Observatorio de Movilidad y Seguridad Vial de la Ciudad de Buenos Aires.

- LinkedIn: [www.linkedin.com/in/sebastian-quintero0413](https://www.linkedin.com/in/sebastian-quintero0413)
- Correo electrónico: [quinterosebastian820@gmail.com](mailto:quinterosebastian820@gmail.com)

Espero que los insights y recomendaciones presentados en este proyecto contribuyan a la toma de decisiones informadas por parte de las autoridades para reducir las víctimas fatales en siniestros viales y mejorar la seguridad vial en la Ciudad de Buenos Aires.
