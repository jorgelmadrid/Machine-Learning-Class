#### Desempeño de un Random Forest

Al momento de resolver un problema de clasificación, las personas encargadas de desarrollar los modelos generalmente se limitan a implementar clasificadores que se encuentran dentro de su área de dominio, sin tener en cuenta otros clasificadores que existen y tienen mejor desempeño. Para esto, los autores del paper *Do we Need Hundreds of Classifiers to Solve Real World Classification Problems?* evaluaron el desempeño de 179 clasificadores diferentes en 121 datasets.

Luego de realizar el análisis en todos los clasificadores, se demostró que el **Parallel Random Forest** es el mejor método para hacer clasificación, incluso cuando es un método antiguo, funciona mejor que clasificadores desarrollados recientemente. Este clasificador alcanzó el indicador más alto de precisión entre los 179 clasificadores evaluados: en promedio alcanza 94% de la precisión máxima en todos los datasets y su precisión promedio en todos los datasets es de 82%. Existen otros clasificadores que tienen un rendimiento bueno en comparación al Parallel Random Forest, dentro de ellos se encuentran: **random forest** utilizando el paquete **randomForest** y afinado con **caret**, **SVM con Gaussian kernel** y **SVM con Poly kernel**.

Sin embargo, al evaluar datasets con dos clases, la red neuronal **avNNet_t** se desempeña mejor que el **Parallel Random Forest**, obteniendo 95% y 94%, respectivamente, en la presión máxima. Los clasificadores restantes, incluyendo otras redes neuronales, arboles de decisión, métodos de ensamblaje como bagging y boosting, vecinos cercanos, modelos lineales generalizados, no son competitivos.

En conclusión, al momento de seleccionar un modelo de clasificación en la vida real, es importante elegir un modelo como línea de base que permita comparar resultados, en este caso, el modelo que se recomienda es Random Forest. Añadiendo que para problemas reales, se cuenta con poco tiempo para tomar la decisión de que modelo utilizar. Comparar uno o dos modelos contra los resultados de un Random Forest, sería suficiente para tomar la decisión. 

**Referencia**

Manuel Fernández-Delgado, Eva Cernadas, Senén Barro and Dinani Amorim. [Do we Need Hundreds of Classifiers to Solve Real World Classification Problems?.](http://jmlr.org/papers/volume15/delgado14a/delgado14a.pdf) *Journal of Machine Learning Research 15, 3133-3181, 2014*
