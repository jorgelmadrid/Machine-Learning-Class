#### ¿Por qué ensemble es una estrategía exitosa en machine learning?

Ensamble es un algoritmo de aprendizaje supervisado en machine learning. que puede ser entrenado y luego utilizado para realizar predicciones. El aprendizaje conjunto o ensemble ayuda a mejorar los resultados de un modelo de machine learning al combinar varios modelos predicitivos en uno solo. Esta técnica ayuda a tener un mejor rendimiento predicitivo comparado con el rendimiento que tendría un solo modelo. Los modelos de ensemble tienen como objetivo disminuir la varianza **(bagging)**, el sesgo **(boosting)** o mejorar las predicciones **(stacking)**.

**1. Bagging:** Abrevación para Bootstrap aggregating, que en español significa muestreo aleatorio con reemplazamiento, consiste en elegir aleatoriamente un número de muestras que serán utilizadas para entrenar el modelo. Bagging incrementa el poder predicitivo del modelo al reducir la varianza, al promediar en conjunto múltiples estimaciones.

**2. Boosting:** Consiste en construir un modelo de ensemble incrementalmente al entrenar nuevos modelos con los datos de training que un modelo previamente clasificó de manera erronea. Luego de esto, las predicciones se combinan mediante voto mayoritario ponderado (Weighted majority vote) para problemas de clasificación y por suma ponderada (Weighted sum) para regresiones. La principal diferencia entre Bagging y Boosting, es que los modelos base son entrenados en secuencia en una version ponderada de la data.

**3. Stacking:** Este método consiste en combinar los diferentes modelos base mediante el aprendizaje de un algoritmo que se encuentra en un segundo nivel. Es decir, todos los otros algoritmos se entrenan usando los datos disponibles, luego un algoritmo combinador se entrena para hacer una predicción final usando todas las predicciones de los otros algoritmos como entradas adicionales.