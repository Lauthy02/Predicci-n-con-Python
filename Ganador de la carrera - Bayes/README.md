# Predicción con Gaussian Naive Bayes - ¿El piloto x va a quedar 1ro en la carrera x?
## El objetivo de estre proyecto es poder predecir si el piloto ingresado va a quedar primero en la carrera ingresada
### Se le podrá pasar al algoritmo una carerrara, la posición 1 y un piloto. El algoritmo arrojará un valor de 1 si predice que va a quedar 1ro o 0 en caso contrario

Para poder predecir esto utilizo el algoritmo Naive Bayes[^1] dentro de la librería scikit-learn, específicamente el objeto `GaussianNB()`.

Los datos son extraidos de 4 csv's, específicamente:
  - [formula1_2019season_raceResults.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/d072131111a2a5135be915d4303df0eb175d3279/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1/formula1_2019season_raceResults.csv)
  - [formula1_2020season_raceResults.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/38cce5eba96603ff1c364d9ba999471a9038b691/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1/formula1_2020season_raceResults.csv)
  - [formula1_2021season_raceResults.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/38cce5eba96603ff1c364d9ba999471a9038b691/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1/formula1_2021season_raceResults.csv)
  - [formula1_2022season_raceResults.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/38cce5eba96603ff1c364d9ba999471a9038b691/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1/formula1_2022season_raceResults.csv)

Estos a estos datos les saqué las columnas que no necesitaba, eliminé las filas con valor NC[^2] en la columna *Position* y cree una columna personalizada llamada *Win* que tiene el valor 1 cuando el valor de la columna Position es 1 y 0 cuando el valor es mayor a 1. De esta manera filtré los 4 csv's mencionados anteriormente y creé un nuevo csv con todos estos datos limpios para poder entrenar al algoritmo [f1_data_limpia_2019_2022.csv](https://github.com/Lauthy02/Prediccion-con-Python/blob/38cce5eba96603ff1c364d9ba999471a9038b691/Ganador%20de%20la%20carrera%20-%20Bayes/csvs_f1_limpios/f1_data_limpia_2019_2022.csv).

Antes de entrenar al algoritmo el csv con todos los datos limpios lo pasé por la función `.dropna()` que limpia los valores nullos que podrían haber quedado.

Una vez entrenado, en otro csv le paso los datos que quiero analizar.

> [!WARNING]
> Los datos a ingresar deben tener el mismo formato que se utilizó al entrenar el algoritmo.

> [!WARNING]
> El valor Position al ingresar los datos siempre debe valer 1.

| Track | Position | Driver |
| --- | --- | --- |
| Monaco | 1 | Fernando Alonso |

# Enlaces
## Información adicional
  - [Formula 1 dataset](https://github.com/toUpperCase78/formula1-datasets)
  - [scikit-learn](https://scikit-learn.org/stable/)
  - [GaussianNB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html#sklearn.naive_bayes.GaussianNB)
  - [Naive Bayes - Wikipedia](https://es.wikipedia.org/wiki/Clasificador_bayesiano_ingenuo)
  - [Naive Bayes usando Python](https://www.aprendemachinelearning.com/?s=bayes)

[^1]: Son una clase especial de algoritmos de clasificación de Aprendizaje Automatico, o Machine Learning. Se basan en una técnica de clasificación estadística llamada “teorema de Bayes”.
[^2]: No clasficado - Not classified
