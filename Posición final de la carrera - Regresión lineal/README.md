# Predicción con Regresión lineal - ¿Cuál va a ser la posición final dependiendo de la posición de salida?
## El objetivo de este proyecto es poder predecir cuál va a ser la posición final dependiendo de la posición de salida
### El programa va a analizar los datos de las carreras del año 2019 

Para poder predecir esto utilizo la regresión lineal.

Los datos son extraidos del csv [formula1_2019season_raceResults.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/d072131111a2a5135be915d4303df0eb175d3279/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1/formula1_2019season_raceResults.csv)

A este csv le saqué las columnas que no necesitaba, eliminé las filas con valor NC[^1] y NQ[^2] en la columna *Position*.

Este csv lo pasé por la función `.dropna()` que limpia los valores nulos que podrían haber quedado. Archivo resultante: [f1_data_limpia_2019.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/5e8bed4690ed95badebc1a0e5605bb4033ae23aa/Posici%C3%B3n%20final%20de%20la%20carrera%20-%20Regresi%C3%B3n%20lineal/csvs_f1_limpios/f1_data_limpia_2019.csv)

Una vez entrenado el algoritmo con los valores limpios, en otro csv escribo los datos que quiero analizar y se los paso.

completar

# Enlaces
## Información adicional
  - [Formula 1 dataset](https://github.com/toUpperCase78/formula1-datasets)
  - [Regresión lineal - Wikipedia](https://es.wikipedia.org/wiki/Regresión_lineal)

[^1]: No clasficado - Not classified
[^2]: ¿?
