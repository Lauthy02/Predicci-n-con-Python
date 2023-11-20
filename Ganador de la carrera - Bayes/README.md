La idea de estre proyecto es poder predecir si x piloto va a ganar la carrera.

Para poder predecir esto utilizo el algoritmo Gaussian Naive Bayes dentro de la librería scikit-learn, específicamente el objeto GaussianNB.

Los datos son extraidos de 4 csv's, específicamente:
-formula1_2019season_raceResults.csv
-formula1_2020season_raceResults.csv
-formula1_2021season_raceResults.csv
-formula1_2022season_raceResults.csv

Estos a estos datos les saqé las columnas que no necesitaba, eliminé las filas con valor 'NC' en la columna Position y cree una columna personalizada llamada 'Win' que tiene el valor 1 cuando el valor de la position es 1 y o cuando es mayor a 1. 

Formula 1 dataset: https://github.com/toUpperCase78/formula1-datasets 
scikit-learn: https://scikit-learn.org/stable/
GaussianNB: https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.GaussianNB.html#sklearn.naive_bayes.GaussianNB
