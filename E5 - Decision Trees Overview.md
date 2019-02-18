#### Tipos de algoritmos de árboles de decisión y sus aplicaciones

**1. ID3 (Iterative Dichotomiser 3)**: Algoritmo inventado por Ross Quinlan para generar un árbol de decisión a partir de un 
conjunto de datos. El algoritmo realiza una búsqueda de arriba hacia abajo, calculando la entropia para cada variable del 
conjunto de datos. Luego, realiza una división en subconjuntos de datos utilizando la variable que minimiza la entropía o
maximiza la ganancia de información. Finalmente, crea un nuevo nodo que contiene la variable seleccionada anteriormente.
En negocios es **utilizado** para predecir el comportamiento de compra de los clientes.

**2. C4.5**: Algoritmo desarrollado por Ross Quinlan. Es una extensión de ID3. C4.5 genera árboles de decisión que se pueden
utilizar para clasificación. Es mejor que ID3 porque soporta variables continuas y discretas y también valores faltantes.
En agricultura es **utilizado** para predecir el grado de calidad del suelo.

**3. CART (Classification and Regression Tree)**: Creado por Breiman en 1984. Puede ser utilizado para construir árboles de 
clasificación y regresión. Utiliza el indice de Gini para seleccionar la variable de división. Es capaz de manejar los valores
faltantes, utilizar cualquier combinación de variables continuas y discretas, seleccionar automáticamente las variables y establecer
interacción entre las variables. En medicina es **utilizado** en transplantes de corazón, para elegir el mejor corazón disponible para
el paciente con las mejores probabilidades de sobrevirir.

**4. CHAID (CHi- squared Automatic Interaction Detector)**: Desarrollado en Sudáfrica y publicado en 1980 por Gordon V. Kass. Es un 
algoritmo basado en pruebas de significancia ajustada (pruebas de Bonferroni). Este algoritmo se puede utilizar para la contrucción 
de árboles de regresión y clasificación. Utiliza divisiones de múltiples vías, por lo tanto necesita tamaños de muestra bastante grandes 
para funcionar de manera efectiva, en grupos de muestras pequeñas, el análisis se puede volver poco confiable. En marketing directo es
**utilizado** para seleccionar grupos de consumidores y predecir cómo sus respuestas a algunas variables afectan otras variables.

**5. MARS (Multivariate adaptive regression splines)**: Creado por Jerome Friedman en 1991. Utilizando una técnica de regresión 
no paramétrica y modelando automáticamente las no linealidades y las interacciones entre variables, es capaz de construir un árbol de regresión. En marketing es **utilizado** para predecir la tasa de respuesta que tendrá una campaña específica.

