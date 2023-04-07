# Predicción de retrasos en vuelos desde el aeropuerto de Santiago (2017)

Este proyecto utiliza datos de vuelos del año 2017 desde el aeropuerto de Santiago junto con datos de nubosidad y precipitaciones de la estación meteorológica del aeropuerto para predecir retrasos en los vuelos. El objetivo es analizar cómo afectan las distintas variables de los vuelos contenidas en `dataset_SCL.csv` , como también las condiciones meteorológicas a la probabilidad de retraso de cada vuelo e incluir estos factores en los modelos predictivos. El análisis se realiza utilizando Python 3 y diversas bibliotecas de ciencia de datos y aprendizaje automático.

Hay dos puntos importantes a considerar en el proyecto:
1. El proyecto se hace basado en el supuesto de que el interés del negocio es desarrollar un modelo que permita predecir retrasos en vuelos con un día de anticipación y comprender qué variables influyen en dichos retrasos. Esto significa que la información de retrasos de vuelos ocurridos en un periodo inferior a 24 horas antes de cada vuelo no debe ser considerada en el análisis.

2. Aunque se utiliza información meteorológica que no se conoce con exactitud en menos de 24 horas de anticipación (dado que el modelo fue entrenado con la información medida en el momento de la fecha y hora programada de cada vuelo), en un escenario hipotético donde se utilice el modelo en producción, se debe tomar en cuenta la información meteorológica pronosticada para la fecha del vuelo en lugar de la información medida.

## Requisitos previos

Para ejecutar este proyecto, necesitarás Python 3.7 o superior y las siguientes bibliotecas:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- plotly.express
- datetime 

Puedes instalar estas bibliotecas utilizando pip:

## Estructura del proyecto

El repositorio del proyecto contiene los siguientes archivos:

- `solution.ipynb`: Cuaderno Jupyter que contiene todo el análisis, la limpieza de datos, la selección de características y la construcción del modelo predictivo.
- `dataset_SCL.csv`: Archivo CSV que contiene los datos de los vuelos desde el aeropuerto de Santiago en 2017.
- `nubosidad_2017.csv`: Cantidad en octas de nubosidad que cubre el cielo medido en la estación meteorológica Pudahuel Santiago, ubicada en el aeropuesto de Santiago. Fuente: https://climatologia.meteochile.gob.cl/application/informacion/fichaDeEstacion/330021
- `precipitaciones_2017.csv`: Cantidad de precipitación líquida caída o acumulada durante un período de 6 Horas medido en la estación meteorológica Pudahuel Santiago, ubicada en el aeropuesto de Santiago. Fuente: https://climatologia.meteochile.gob.cl/application/informacion/fichaDeEstacion/330021
- `synthetic_features.csv`: Archivo de respuesta challenge 2.
- `Santiago_Valdivieso.pdf`: CV del autor.
- `README.md`: Archivo que proporciona información sobre el proyecto y las instrucciones para ejecutarlo.

## Ejecución del proyecto

Para ejecutar el proyecto, sigue estos pasos:

1. Clona el repositorio en tu computadora local:
2. Navega hasta la carpeta del repositorio clonado en tu computadora.
3. Abre el cuaderno Jupyter `solution.ipynb` utilizando Jupyter Notebook o JupyterLab:
4. Ejecuta todas las celdas del cuaderno desde el principio hasta el final para ver el proyecto completo.
