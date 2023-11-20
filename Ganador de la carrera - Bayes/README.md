# Predicción con Gaussian Naive Bayes - ¿El piloto x va a quedar 1ro en la carrera x?
## El objetivo de estre proyecto es poder predecir si x piloto va a quedar primero en x carrera
### Se le podrá pasar al algoritmo una carerrara *Monaco*, la posición *1* y un piloto *Fernando Alonso* y el algoritmo arrojará un valor de 1 si predice que va a quedar 1ro o 0 en caso contrario.

Para poder predecir esto utilizo el algoritmo Naive Bayes[^1] dentro de la librería scikit-learn, específicamente el objeto GaussianNB.

Los datos son extraidos de 4 csv's, específicamente:
  - formula1_2019season_raceResults.csv
  - formula1_2020season_raceResults.csv
  - formula1_2021season_raceResults.csv
  - formula1_2022season_raceResults.csv

Estos a estos datos les saqué las columnas que no necesitaba, eliminé las filas con valor 'NC' en la columna Position y cree una columna personalizada llamada 'Win' que tiene el valor 1 cuando el valor de la columna Position es 1 y 0 cuando el valor es mayor a 1.

De esta manera filtré los 4 csv's mencionados anteriormente y creé uno nuevo con todos estos datos limpios para poder entrenar al algoritmo.

# Enlaces
## Información adicional
  - [Formula 1 dataset](https://github.com/toUpperCase78/formula1-datasets)
  - [scikit-learn](https://scikit-learn.org/stable/)
  - [GaussianNB](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html#sklearn.naive_bayes.GaussianNB)
  - [Naive Bayes - Wikipedia](https://es.wikipedia.org/wiki/Clasificador_bayesiano_ingenuo)
  - [Naive Bayes usando Python](https://www.aprendemachinelearning.com/?s=bayes)

[^1]: Son una clase especial de algoritmos de clasificación de Aprendizaje Automatico, o Machine Learning. Se basan en una técnica de clasificación estadística llamada “teorema de Bayes”.
