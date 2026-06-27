# TFM - Análisis del rendimiento colectivo e individual de un equipo de fútbol mediante técnicas Big Data

Este repositorio contiene el código, los datos y las visualizaciones desarrolladas para el análisis del rendimiento colectivo e individual de un equipo de fútbol mediante técnicas Big Data.

El objetivo principal del proyecto es analizar el rendimiento de equipos y jugadores desde una perspectiva colectiva, individual y predictiva. Para ello, se emplean datos futbolísticos estructurados, técnicas de limpieza y transformación de datos, análisis exploratorio, modelos de aprendizaje automático y un dashboard interactivo desarrollado en Power BI.

## Estructura del repositorio

```text
TFM/
│
├── DATA/
│   └── Datasets utilizados en el proyecto
│
├── comparativa_madrid.ipynb
│   └── Notebook de análisis exploratorio y comparativo
│
├── modelo.ipynb
│   └── Notebook de modelado predictivo
│
├── visualizacion_madrid_barca.pbix
│   └── Dashboard interactivo desarrollado en Power BI
│
└── README.md
    └── Descripción general del proyecto
```

## Descripción de los archivos

### `DATA/`

La carpeta `DATA` contiene los conjuntos de datos utilizados en el desarrollo del trabajo. Estos datos sirven como base para el análisis exploratorio, la comparación entre equipos, la creación de variables y el entrenamiento de los modelos predictivos.

Los datos utilizados incluyen información relacionada con partidos, equipos, jugadores, temporadas, resultados y estadísticas de rendimiento futbolístico. A partir de estos datos se construyen distintas variables de análisis, tanto para la parte descriptiva como para la parte predictiva del proyecto.

### `comparativa_madrid.ipynb`

Este notebook contiene la parte de análisis exploratorio y comparativo del proyecto. En él se realiza la carga, limpieza y transformación inicial de los datos, así como el estudio de diferentes variables relacionadas con el rendimiento futbolístico.

El análisis se centra principalmente en la comparación de equipos, temporadas y estadísticas relevantes, con especial atención al rendimiento del Real Madrid y del FC Barcelona. A través de este notebook se generan tablas, métricas y gráficos que permiten estudiar diferencias de rendimiento, evolución temporal y patrones asociados al comportamiento deportivo de los equipos.

Entre las tareas realizadas en este archivo se incluyen:

* Carga de los datasets desde la carpeta `DATA`.
* Limpieza y preparación de los datos.
* Análisis exploratorio de variables futbolísticas.
* Comparación entre equipos y temporadas.
* Generación de gráficos y visualizaciones iniciales.
* Obtención de conclusiones descriptivas para apoyar el análisis posterior.

### `modelo.ipynb`

Este notebook contiene la fase predictiva del Trabajo Fin de Máster. En él se preparan los datos para entrenar distintos modelos de aprendizaje automático con el objetivo de estimar el resultado de los partidos y analizar la capacidad predictiva de diferentes algoritmos.

En esta fase se comparan varios modelos de clasificación, entre ellos:

* Regresión logística.
* Árbol de decisión.
* Random Forest.
* Gradient Boosting.

Los modelos se entrenan y evalúan utilizando métricas como `accuracy`, `precision`, `recall`, `F1-score` y matriz de confusión. Además, se emplea `GridSearchCV` para seleccionar la mejor configuración de hiperparámetros.

El modelo que obtiene el mejor rendimiento global es la regresión logística multiclase, configurada con un parámetro de regularización `C = 1`, un máximo de 5.000 iteraciones y el algoritmo de optimización `LBFGS`. La selección de esta configuración se realiza mediante validación cruzada de 5 particiones, utilizando la métrica `accuracy` como criterio de evaluación.

A partir de las probabilidades generadas por el modelo, se calculan probabilidades de victoria local, empate y victoria visitante. Posteriormente, estas probabilidades se transforman en puntos esperados, lo que permite simular escenarios futuros y obtener una clasificación estimada.

### `visualizacion_madrid_barca.pbix`

Este archivo contiene el dashboard interactivo desarrollado en Power BI. Su finalidad es facilitar la interpretación visual de los resultados obtenidos durante el análisis.

El panel permite explorar la información de forma dinámica mediante filtros e indicadores visuales. A través del dashboard se pueden comparar equipos, temporadas, posiciones y jugadores, integrando la información procedente de los distintos datasets utilizados en el proyecto.

El uso de Power BI permite presentar los resultados de forma clara, visual e interactiva, facilitando la toma de decisiones basada en datos y complementando los análisis realizados en Python.

## Fuentes de datos

Los datos utilizados en este proyecto proceden de datasets futbolísticos estructurados almacenados en la carpeta `DATA`. Estos conjuntos de datos incluyen información histórica sobre partidos, equipos, jugadores, resultados y estadísticas de rendimiento.

Las fuentes empleadas corresponden a datos públicos y abiertos relacionados con competiciones futbolísticas, recopilados y organizados para su posterior análisis mediante Python y Power BI. Estos datos permiten estudiar el rendimiento deportivo desde diferentes perspectivas: evolución temporal, comparación entre equipos, análisis de jugadores y predicción de resultados.

En concreto, el proyecto utiliza datos relativos a:

* Resultados de partidos.
* Estadísticas de equipos.
* Estadísticas de jugadores.
* Temporadas y competiciones.
* Variables de rendimiento deportivo.
* Información necesaria para la creación del modelo predictivo.

Los datasets originales se encuentran en la carpeta `DATA`, desde donde son cargados por los notebooks para realizar el tratamiento, análisis y modelado.

## Herramientas utilizadas

Para el desarrollo del proyecto se han utilizado las siguientes herramientas y librerías:

* Python.
* Pandas.
* NumPy.
* Matplotlib.
* Seaborn.
* Scikit-learn.
* Power BI.
* Jupyter Notebook.
* GitHub.


## Objetivo del proyecto

El objetivo general del proyecto es aplicar técnicas de Big Data, Visual Analytics y aprendizaje automático al análisis del rendimiento futbolístico. El trabajo busca complementar las métricas tradicionales con herramientas analíticas que permitan identificar patrones, comparar comportamientos entre equipos y estimar escenarios futuros a partir del rendimiento histórico.

## Autor

**Jorge González Álvarez**
Trabajo Fin de Máster - Big Data y Visual Analytics
