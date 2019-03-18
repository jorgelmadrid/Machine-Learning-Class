# E12 - Gradient Boosting Review

Principales diferencias entre los algoritmos implementados en Gradient Boosting Classifier y XGB Classifier:

En **Gradient Boosting Classifier** se implementa el algoritmo *Boosting*, que consiste en una técnica secuencial basada en el principio de aprendizaje conjunto: se construye el modelo incrementalmente al entrenar nuevos modelos con los datos de training que un modelo previamente clasificó de manera errónea, mejorando la precisión en la predicción. En este caso, los resultados predichos correctamente reciben un peso menor mientras que los resultados mal clasificados reciben un peso mayor.

**XGBoost (eXtreme Gradient Boosting)**: es una implementación avanzada del algoritmo Gradient Boosting, a diferencia de esta implementación, XGBoost es capaz de:

1. Reducir el sobreajuste (overfitting) al tener regularización, de hecho, XGBoost también se conoce como técnica de "aumento regularizado".

2. Implementar procesamiento en paralelo al realizar la búsqueda de la partición a cada nivel por feature. Además, es mucho más rápido que el algoritmo Gradient Boosting y soporta implementación en Hadoop.  

3. Manejar valores faltantes (missing values): El usuario debe proporcionar un valor diferente al de otras observaciones y pasarlo como un parámetro. XGBoost encuentra un valor faltante en cada nodo y aprende qué ruta tomar para los valores faltantes en el futuro.

4. Realizar validación cruzada (Cross-Validation): la validación viene incorporada en el algoritmo, XGBoost permite al usuario ejecutar una validación cruzada en cada iteración del proceso de Boosting y, por lo tanto, es fácil obtener el número óptimo exacto de iteraciones de Boosting en una sola ejecución. Esto es diferente a Gradient Boosting, donde tenemos que ejecutar una búsqueda de cuadrícula (grid-search) y solo se pueden probar unos valores limitados.

5. Crecer el árbol hasta el max_depth especificado, logrando dividir un nodo incluso cuando no encuentra una ganancia positiva en la división para luego podar el árbol hacia atrás y eliminar las divisiones en las que no hay ganancias positivas. Algunas veces una partición del árbol con pérdida negativa, por ejemplo -2, puede ir seguida de una partición del árbol con pérdida positiva +10. Gradient Boosting se detendría cuando se encontrara con -2. Pero XGBoost irá más profundo y verá un efecto combinado de +8 de la división y mantendrá ambos.
