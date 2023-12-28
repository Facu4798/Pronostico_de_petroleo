# Pronóstico de petróleo y gas en la Argentina

En este trabajo se realiza un análisis de serie de tiempo de la producción primaria de petróleo y la producción de gas de baja presión para poder predecir sus valores hasta diciembre de 2024 teniendo datos hasta junio de 2023. Los datos fueron extraidos de [datos.gob.ar](https://www.datos.gob.ar/hu/dataset/energia-produccion-petroleo-gas-sesco).

El trabajo se desarrolló de la siguiente manera: se realizó un promedio móvil de los datos para luego obtener una tendencia mediante una regresión no lineal univariada. Seguido de esto se obtuvieron los factores estacionales para cada mes y estos se utilizaron para realizar una predicción de la forma $predicción_i = tendencia(tiempo) * factor_i $. Luego de esto, se obtuvo el error aleatorio $\sigma$ para realizar las mencionadas predicciones dentro de un intervalo de confianza con una confianza del 95%.Por último se realizó una regresión para determinar si existía una relación lineal entre ambas variables, y reemplazar las predicciones en funció  de esta. Al no haber relación lineal, se mantuvieron las predicciones de la forma antes mencionada.

Para mas información, refierase al pdf en este repositorio.

El codigo se encuentra en la siguiente notebook de [google colab](https://colab.research.google.com/drive/118GUlkWZm9VXB47SZh4HtCUloRhFJ6A4#scrollTo=ftZ7bSezT4nL) o en el mismo notebook $ipynb$ subido a este repositorio
