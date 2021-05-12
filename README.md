# 2.Programacion_y_NUMPY

## Cuando Python no alcanza, aparecen las librerías

A veces, las estructuras de datos que vienen con Python —y sus funcionalidades asociadas— no son suficientes para lo que queremos hacer, como por ejemplo tomar una lista de números y sumarles un valor a ellos:

![image](https://user-images.githubusercontent.com/80594428/117992449-54017980-b315-11eb-8648-ea3e58611358.png)

Por ello, existen complementos que podemos sumarle a nuestro lenguaje de programación que se llaman librerías o bibliotecas. Una librería es, en el fondo, funcionalidades que otras personas programaron y que nosotros sumamos a nuestro espacio de trabajo para aprovecharlas.

NumPy (proveniente de Numerical Python), es la librería por defecto para hacer operaciones numéricas de manera eficiente en Python y viene con una estructura de datos propia: los arrays o arreglos.

Un arreglo, a primer orden, es como una lista. De hecho, se pueden crear a partir de una lista. Pero hay una diferencia crucial es que, mientras las listas pueden contener dentro cualquier tipo de dato básico, los arreglos funcionan mejor cuando lo que contiene son solamente números.

## Un poco más de programación: Operaciones lógicas
Las operaciones lógicas son aquellas que dan como resultado un booleano. Recordemos que un booleano es un tipo de dato básico que puede tomar dos valores, Verdadero (True) o Falso (False). En general, los usamos como condiciones para tomar decisiones en el flujo de programación.

# Introducción a NumPy
No importa cuáles sean los datos, el primer paso para que sean analyzables será transformarlos en matrices de números. (Discutiremos algunos ejemplos específicos de este proceso más adelante en Ingeniería de Características)

El almacenamiento eficiente y la manipulación de matrices numéricas es absolutamente fundamental para el proceso de hacer ciencia de datos.

## Descripción de los tipos de datos en Python

Una lista de Python es algo más que una lista: la ventaja de la lista es la flexibilidad, dado que cada elemento de lista es una estructura completa que contiene información de datos y tipos, la lista se puede rellenar con datos de cualquier tipo deseado. Las matrices de estilo NumPy de tipo fijo carecen de esta flexibilidad, pero son mucho más eficaces para almacenar y manipular datos.

Matrices de tipo fijo en Python: se puede utilizar para crear matrices densas de un tipo uniforme:array
Creación de matrices a partir de listas de Python:  podemos usar para crear matrices a partir de listas de Python: np.array. Recuerde que, a diferencia de las listas de Python, NumPy está restringido a matrices que contienen el mismo tipo.

Si queremos establecer explícitamente el tipo de datos de la matriz resultante, podemos usar la palabra clave:dtype

![image](https://user-images.githubusercontent.com/80594428/117995145-785e5580-b317-11eb-8124-ad115b4acdfe.png)
 
las matrices NumPy pueden ser explícitamente multidimensionales; aquí hay una manera de inicializar una matriz multidimensional utilizando una lista de listas, donde las listas internas se tratan como filas de la matriz bidimensional resultante.
 
  ![image](https://user-images.githubusercontent.com/80594428/117995219-87dd9e80-b317-11eb-80b8-1e52ecbc7f56.png)
 
Creación de matrices desde cero:
	array de 10 ceros:

 ![image](https://user-images.githubusercontent.com/80594428/117995245-8e6c1600-b317-11eb-9dfd-2f70a34caa60.png)
 
	array float de 3x5 relleno de unos:

 ![image](https://user-images.githubusercontent.com/80594428/117995285-94fa8d80-b317-11eb-8868-4962d32cf7aa.png)

	array 3x5 rellana con el numero 3.14:

 ![image](https://user-images.githubusercontent.com/80594428/117995372-a6439a00-b317-11eb-8add-b24ce308778c.png)

	array con una secuencia lineal, que empiece con 0 termine en 20 y vaya de 2 en 2:
 
![image](https://user-images.githubusercontent.com/80594428/117995400-ab084e00-b317-11eb-918f-d5d4e5f61787.png)

	array de cinco valores espaciados entre el 0 y 1

 ![image](https://user-images.githubusercontent.com/80594428/117995458-b78ca680-b317-11eb-90e6-091705bed879.png)

	array de 3x3 de distribución uniforme, aleatoria de valores entre 0 y 1

 ![image](https://user-images.githubusercontent.com/80594428/117995510-c2473b80-b317-11eb-8a85-045cdb66878c.png)

	array de 3x3 de distribución normal, aleatoria, con mean = 0 ans std= 1

 ![image](https://user-images.githubusercontent.com/80594428/117995819-033f5000-b318-11eb-8d13-316c0f6a78af.png)

	array de 3x3 de aleatorios int en el intervalo de [0,10]

 ![image](https://user-images.githubusercontent.com/80594428/117995779-fb7fab80-b317-11eb-95e8-08fd97b08fc2.png)

	Crear una matriz identidad (Matriz Identidad: matriz cuadrada con valores 1 en la diago nal principal y el resto de valores igual a 0)

 ![image](https://user-images.githubusercontent.com/80594428/117995928-18b47a00-b318-11eb-9c0e-19a066b939ad.png)

	Array no iniciada con 3 enteros

 ![image](https://user-images.githubusercontent.com/80594428/117996010-29fd8680-b318-11eb-9b1d-ceb6aec6b937.png)

## Los conceptos básicos de NumPy Arrays

Cubriremos algunas categorías de manipulaciones básicas de arreglos de discos aquí:

•	Atributos de matrices: determinación del tamaño, la forma, el consumo de memoria y los tipos de datos de las matrices

•	Indexación de matrices: obtener y establecer el valor de los elementos de matriz individuales

•	Corte de matrices: Conseguir y configurar subarrays más pequeños dentro de una matriz más grande

•	Remodelación de matrices: cambiar la forma de una matriz determinada

•	Unión y división de matrices: combinar varias matrices en una sola y dividir una matriz en muchos

Atributos de matriz NumPy: Comenzaremos definiendo tres matrices aleatorias, una matriz unidimensional, bidimensional y tridimensional. Usaremos el generador de números aleatorios de NumPy, que sembraremos con un valor establecido con el fin de garantizar que se generen las mismas matrices aleatorias cada vez que se ejecute este código:

![image](https://user-images.githubusercontent.com/80594428/117996598-a8f2bf00-b318-11eb-8907-a6ae5f8aa3af.png)
 
Indexación de matrices: acceso a elementos únicos: En una matriz unidimensional, se puede acceder al valor $i^{th}$ (contando desde cero) especificando el índice deseado entre corchetes, al igual que con las listas de Python:

![image](https://user-images.githubusercontent.com/80594428/117996625-af813680-b318-11eb-8548-f4db6e33c807.png)

![image](https://user-images.githubusercontent.com/80594428/117996785-d2abe600-b318-11eb-94e7-0931d0534a39.png)

En una matriz multidimensional, se puede acceder a los elementos mediante una tupla de índices separada por comas:

![image](https://user-images.githubusercontent.com/80594428/117996819-db042100-b318-11eb-8fc5-bb51f39ff2a9.png)
 
Los valores también se pueden modificar utilizando cualquiera de las notación de índice anteriores:

![image](https://user-images.githubusercontent.com/80594428/117996853-e48d8900-b318-11eb-958a-e40f60698bfe.png)
 
Tenga en cuenta que, a diferencia de las listas de Python, las matrices NumPy tienen un tipo fijo. Esto significa, por ejemplo, que si intenta insertar un valor de punto flotante en una matriz de enteros, el valor se truncará silenciosamente.
 
![image](https://user-images.githubusercontent.com/80594428/117996890-ebb49700-b318-11eb-949e-153b9c745b8b.png)

Corte de matriz: Acceso a Subarrays: también podemos usar corchetes para acceder a subarrays con la notación de sector, marcada por el carácter de dos puntos ().

![image](https://user-images.githubusercontent.com/80594428/117997900-c8d6b280-b319-11eb-9c3f-f591922bfd4b.png)

	Subarrays unidemensionales:
 
![image](https://user-images.githubusercontent.com/80594428/117997948-d2f8b100-b319-11eb-9f69-ee9ff794a34f.png)

![image](https://user-images.githubusercontent.com/80594428/117997982-d8ee9200-b319-11eb-99c4-72530138d10b.png)

Un caso potencialmente confuso es cuando el valor es negativo. En este caso, los valores predeterminados para y se intercambian. Esto se convierte en una forma conveniente de invertir una matriz: step:start:stop
 
![image](https://user-images.githubusercontent.com/80594428/117998110-f7ed2400-b319-11eb-86fc-eeaf3b742e62.png)

	Subarrays multidimensionales: funcionan de la misma manera, con varios sectores separados por comas. Por ejemplo:

![image](https://user-images.githubusercontent.com/80594428/117998208-0d624e00-b31a-11eb-88f8-f3dd51e2bdb3.png)

Por último, las dimensiones de la subarray incluso se pueden invertir juntas:

![image](https://user-images.githubusercontent.com/80594428/118001365-0ee14580-b31d-11eb-98c7-0f70a170b551.png)

  o	Acceso a filas y columnas de matriz: Esto se puede hacer combinando indexación y corte, utilizando un sector vacío marcado por un solo punto ()::

![image](https://user-images.githubusercontent.com/80594428/118001412-17398080-b31d-11eb-85e0-e92f2ac0f01d.png)

En el caso del acceso a filas, el sector vacío se puede omitir para una sintaxis más compacta:

![image](https://user-images.githubusercontent.com/80594428/118001794-70a1af80-b31d-11eb-853b-3097649e7e89.png)

	Subarrays como vistas sin copia: Una cosa importante y extremadamente útil para saber acerca de los sectores de matriz es que devuelven vistas en lugar de copias de los datos de la matriz. Este es un área en la que el corte de la matriz NumPy difiere del corte de la lista de Python: en las listas, los sectores serán copias. Considere nuestra matriz bidimensional desde antes:

![image](https://user-images.githubusercontent.com/80594428/118001871-81eabc00-b31d-11eb-93dc-75acc7f7b14e.png)

Vamos a extraer un 2x2 subarray de esto:

![image](https://user-images.githubusercontent.com/80594428/118001896-87480680-b31d-11eb-8a4d-dcd3b1fd3b3d.png)

¡Ahora bien, si modificamos este subarray, veremos que la matriz original ha cambiado! Observar:

![image](https://user-images.githubusercontent.com/80594428/118001946-8f07ab00-b31d-11eb-98ed-f30e9e1417c4.png)

Este comportamiento predeterminado significa que cuando trabajamos con conjuntos de datos grandes, podemos acceder y procesar fragmentos de estos conjuntos de datos sin necesidad de copiar el búfer de datos subyacente.

	Creación de copias de matrices: a veces es útil copiar explícitamente los datos dentro de una matriz o un subarray. Esto se puede hacer más fácilmente con el método:copy()

![image](https://user-images.githubusercontent.com/80594428/118002039-a181e480-b31d-11eb-978d-149e79cc0987.png)

Si ahora modificamos este subarray, la matriz original no se toca:

![image](https://user-images.githubusercontent.com/80594428/118002076-a9da1f80-b31d-11eb-8999-90e5b9bacc19.png)
 
Remodelación de matrices: a forma más flexible de hacerlo es con el método. Por ejemplo, si desea colocar los números del 1 al 9 en una cuadrícula de $3 \times 3$, puede hacer lo siguiente: reshape

![image](https://user-images.githubusercontent.com/80594428/118002322-e3ab2600-b31d-11eb-89a7-6315f28b4aec.png)

Para que esto funcione, el tamaño de la matriz inicial debe coincidir con el tamaño de la matriz remodelada.

![image](https://user-images.githubusercontent.com/80594428/118002351-e9a10700-b31d-11eb-987c-26825a6701b7.png)
 
![image](https://user-images.githubusercontent.com/80594428/118002471-04737b80-b31e-11eb-945b-67c26f0971b9.png)

Concatenación y división de matrices: También es posible combinar varias matrices en una sola y, por el contrario, dividir una sola matriz en varias matrices.

	Concatenación de matrices: se realiza principalmente mediante las rutinas, y. toma una tupla o lista de matrices como su primer argumento, como podemos ver aquí: np.concatenate np.vstack np.hstack np.concatenate

![image](https://user-images.githubusercontent.com/80594428/118002510-0e957a00-b31e-11eb-88a1-9575b67628be.png)

o	Concatenar más de dos matrices a la vez:

![image](https://user-images.githubusercontent.com/80594428/118002557-1d7c2c80-b31e-11eb-9c69-c61940abac67.png)

o	Concatenar matrices bidimensionales

![image](https://user-images.githubusercontent.com/80594428/118002596-27059480-b31e-11eb-8a75-200303502a82.png)

o	Concatenar matrices de dimensiones mixtas: puede ser más claro utilizar las funciones (pila vertical) y (pila horizontal): np.vstack np.hstack

![image](https://user-images.githubusercontent.com/80594428/118002627-2ff66600-b31e-11eb-8e02-90455a1ea4d1.png)

Similarmente, apilará matrices a lo largo del tercer eje. np.dstack

	División de matrices: Lo contrario de la concatenación es la división. Para cada uno de ellos, podemos pasar una lista de índices que dan los puntos divididos:np.split np.hsplit np.vsplit
o	Np.split

![image](https://user-images.githubusercontent.com/80594428/118003217-c3c83200-b31e-11eb-9d6c-d2efb9f4c8cc.png)

o	Funciones Y relacionadas:

![image](https://user-images.githubusercontent.com/80594428/118003261-cb87d680-b31e-11eb-9ab7-7d0e83678a40.png)

![image](https://user-images.githubusercontent.com/80594428/118003336-de021000-b31e-11eb-921c-b99cd26981b3.png)

# Cálculo en matrices NumPy: funciones universales

Esta sección motiva la necesidad de los ufuncs de NumPy, que se pueden utilizar para hacer que los cálculos repetidos en los elementos de matriz sean mucho más eficientes. A continuación, introduce muchos de los ufuncs aritméticos más comunes y útiles disponibles en el paquete NumPy.

## Explorando los UFuncs de NumPy

	Aritmética de array

![image](https://user-images.githubusercontent.com/80594428/118003918-5ff23900-b31f-11eb-8d75-35348de52272.png)

	Valor absoluto

![image](https://user-images.githubusercontent.com/80594428/118003982-6c769180-b31f-11eb-9c39-3643f7104f97.png)

Características avanzadas de Ufunc:

	Especificación de salida: especifica la matriz donde se almacenará el resultado del cálculo usando el argumento de la función:out

![image](https://user-images.githubusercontent.com/80594428/118004051-7ef0cb00-b31f-11eb-879e-14b09887e0b9.png)

	Agregados: si queremos reducir una matriz con una operación determinada, podemos usar el método de cualquier ufunc. Una reducción aplica repetidamente una operación determinada a los elementos de una matriz hasta que solo queda un solo resultado. Reduce	

o	amar al ufunc devuelve la suma de todos los elementos de la matriz: reduce add

![image](https://user-images.githubusercontent.com/80594428/118004124-92039b00-b31f-11eb-8608-de685e81e7e0.png)

o	llamar al ufunc se da como resultado el producto de todos los elementos de matriz: reduce multiply

![image](https://user-images.githubusercontent.com/80594428/118004148-9760e580-b31f-11eb-9014-0eec08d0772c.png)

o	Si queremos almacenar todos los resultados intermedios del cálculo, podemos usar: accumulate

![image](https://user-images.githubusercontent.com/80594428/118004221-a5af0180-b31f-11eb-9bbc-8c08a6a47274.png)

	Productos externos: puede calcular la salida de todos los pares de dos entradas diferentes utilizando el método. Permite, en una línea, hacer cosas como crear una tabla de multiplicación: outer
 
![image](https://user-images.githubusercontent.com/80594428/118004271-af386980-b31f-11eb-8b35-e3b99711a363.png)

## Agregaciones: Min, Max y Everything In Between

Las estadísticas de resumen más comunes son la desviación media y estándar, que le permiten resumir los valores "típicos" en un conjunto de datos, pero otros agregados también son útiles (la suma, producto, mediana, mínimo y máximo, cuantiles, etc.).

Sumando los valores de una matriz: calcula la suma de todos los valores de una matriz. sum

![image](https://user-images.githubusercontent.com/80594428/118004331-c1b2a300-b31f-11eb-9ff2-90eb3befabb2.png)

![image](https://user-images.githubusercontent.com/80594428/118004350-c4ad9380-b31f-11eb-83f3-b85705eb4e37.png)
 
Es más eficiente usar sum() que np.sum()

Mínimo y Máximo: para encontrar el valor mínimo y el valor máximo de cualquier matriz determinada: min max

![image](https://user-images.githubusercontent.com/80594428/118004483-e0b13500-b31f-11eb-8dd3-e82b69777d06.png)

Para estos y varios otros agregados NumPy, una sintaxis más corta es utilizar métodos del propio objeto de matriz:min max sum

![image](https://user-images.githubusercontent.com/80594428/118004524-ea3a9d00-b31f-11eb-97a8-62c84a7e2ec9.png)

	Agregados multidimensionales: Un tipo común de operación de agregación es un agregado a lo largo de una fila o columna. Supongamos que tiene algunos datos almacenados en una matriz bidimensional:

![image](https://user-images.githubusercontent.com/80594428/118004564-f32b6e80-b31f-11eb-803d-3bece309cbf7.png)

Las funciones de agregación toman un argumento adicional que especifica el eje a lo largo del cual se calcula el agregado. Por ejemplo, podemos encontrar el valor mínimo dentro de cada columna especificando: axis=0

![image](https://user-images.githubusercontent.com/80594428/118004595-f9214f80-b31f-11eb-8cf4-097ab7e0acfc.png)

Del mismo modo, podemos encontrar el valor máximo dentro de cada fila:

![image](https://user-images.githubusercontent.com/80594428/118004617-fcb4d680-b31f-11eb-8963-62fec7263098.png)

	Otras funciones de agregación:

![image](https://user-images.githubusercontent.com/80594428/118004630-01798a80-b320-11eb-9772-a145b61a3a2c.png)

# Comparaciones, máscaras y lógica booleana

## Operadores de comparación como ufuncs

![image](https://user-images.githubusercontent.com/80594428/118005131-7f3d9600-b320-11eb-8760-ba09f4a398ca.png)

![image](https://user-images.githubusercontent.com/80594428/118005144-82388680-b320-11eb-9391-b59cfa34ebad.png)

Trabajar con matrices booleanas

	Recuento de Entradas: Para contar el número de entradas de una matriz booleana, es útil: True np.count_nonzero

![image](https://user-images.githubusercontent.com/80594428/118005205-8ebcdf00-b320-11eb-8918-5a69c70cf874.png)

Otra forma de obtener esta información es utilizar: np.sum False 0 True 1

![image](https://user-images.githubusercontent.com/80594428/118005224-92e8fc80-b320-11eb-9612-a36eb4a75732.png)

Si estamos interesados en comprobar rápidamente si alguno o todos los valores son verdaderos, podemos usar: np.any np.all

![image](https://user-images.githubusercontent.com/80594428/118005240-98464700-b320-11eb-86be-fcdcf907b484.png)
 
![image](https://user-images.githubusercontent.com/80594428/118005257-9d0afb00-b320-11eb-9cd7-b6862c276b91.png)

![image](https://user-images.githubusercontent.com/80594428/118005288-a3997280-b320-11eb-8848-2343b21540aa.png)

	Operadores Booleanos

![image](https://user-images.githubusercontent.com/80594428/118005332-aac08080-b320-11eb-8d4f-2278c67b1919.png)

Usando estas herramientas, podríamos empezar a responder a los tipos de preguntas que tenemos sobre nuestros datos. Algunos ejemplos de resultados que podemos calcular al combinar máscaras con agregaciones:

![image](https://user-images.githubusercontent.com/80594428/118005395-ba3fc980-b320-11eb-94f7-234959226858.png)

  Así podemos ver que hay 29 días con precipitaciones entre 0.5 y 1.0 pulgadas (tener en cuenta que los paréntesis aquí son importantes):
 
![image](https://user-images.githubusercontent.com/80594428/118005445-c75cb880-b320-11eb-98c8-0b8415be834a.png)

Usando la equivalencia de A Y B y NOT (NO A O NO B), podemos calcular el mismo resultado de una manera diferente:
 
![image](https://user-images.githubusercontent.com/80594428/118005486-cfb4f380-b320-11eb-9373-3f4393c1177a.png)

Aparte: Uso de las palabras clave y/o versus los operadores &/|
‘’and’’ realiza una única evaluación booleana en un objeto completo, mientras que ‘’&’’ realiza varias evaluaciones booleanas en el contenido (los bits individuales o bytes) de un objeto. Para las matrices NumPy booleanas, esta última es casi siempre la operación deseada.andor&|
 
![image](https://user-images.githubusercontent.com/80594428/118005517-d6436b00-b320-11eb-9beb-5f2ca58a535f.png)

![image](https://user-images.githubusercontent.com/80594428/118005529-d93e5b80-b320-11eb-94fc-556a747848f5.png)

# Fancy Index

La indexación de lujo es como la simple indexación que ya hemos visto, pero pasamos matrices de índices en lugar de scalars individuales. Esto nos permite acceder y modificar muy rápidamente subconjuntos complicados de los valores de una matriz. arr[0] arr[:5] arr[arr > 0]

## Explorando la Fancy Index

Significa pasar una matriz de índices para acceder a varios elementos de matriz a la vez. Por ejemplo, considere la siguiente matriz:
 
![image](https://user-images.githubusercontent.com/80594428/118005721-0428af80-b321-11eb-9408-8d0aeae0548f.png)

![image](https://user-images.githubusercontent.com/80594428/118005757-0ab72700-b321-11eb-9102-f0e7e6a32643.png)

Alternativamente, podemos pasar una sola lista o matriz de índices para obtener el mismo resultado:

![image](https://user-images.githubusercontent.com/80594428/118005792-130f6200-b321-11eb-9722-01f65aa47a8c.png)

Al utilizar la indexación de lujo, la forma del resultado refleja la forma de las matrices de índice en lugar de la forma de la matriz que se está indexando:
 
![image](https://user-images.githubusercontent.com/80594428/118005811-16a2e900-b321-11eb-843d-37bec79c4892.png)

# Sorting Arrays

## Clasificación rápida en NumPy: y np.sortnp.argsort

Para la mayoría de las aplicaciones, el quicksort predeterminado es más que suficiente.sort sorted np.sort np.sorted

Para devolver una versión ordenada de la matriz sin modificar la entrada, puede utilizar: np.sort

![image](https://user-images.githubusercontent.com/80594428/118005893-2b7f7c80-b321-11eb-9027-6ec3020f7c49.png)

Si prefiere ordenar la matriz in situ, puede utilizar el método de matrices: sort

![image](https://user-images.githubusercontent.com/80594428/118006399-9c269900-b321-11eb-8b89-edcdc454f0b7.png)

Una función relacionada es, que en su lugar devuelve los índices de los elementos ordenados: argsort

![image](https://user-images.githubusercontent.com/80594428/118006450-a47ed400-b321-11eb-8ebf-b7e66c671678.png)

Estos índices se pueden utilizar (a través de la fancy indexación) para construir la matriz ordenada si lo desea:

![image](https://user-images.githubusercontent.com/80594428/118006477-ab0d4b80-b321-11eb-9502-b946bca40cef.png)

## Ordenar a lo largo de filas o columnas

Mediante el argumento: axis. Tener en cuenta que esto trata cada fila o columna como una matriz independiente, y cualquier relación entre los valores de fila o columna se perderá.

![image](https://user-images.githubusercontent.com/80594428/118006517-b3658680-b321-11eb-8ec3-3d8342e60cf8.png)

![image](https://user-images.githubusercontent.com/80594428/118006534-b791a400-b321-11eb-9b87-cf516dfdc3a4.png)

## Ordenaciones parciales: Particionamiento

A veces simplemente queremos encontrar los valores k más pequeños de la matriz. NumPy proporciona esto en la función. np.partition toma una matriz y un número K; el resultado es una nueva matriz.

![image](https://user-images.githubusercontent.com/80594428/118006578-c11b0c00-b321-11eb-85ec-82e8697e176c.png)

Tenga en cuenta que los tres primeros valores de la matriz resultante son los tres más pequeños de la matriz y las posiciones restantes de la matriz contienen los valores restantes.

De forma similar a la ordenación, podemos particionar a lo largo de un eje arbitrario de una matriz multidimensional:

![image](https://user-images.githubusercontent.com/80594428/118006620-c8dab080-b321-11eb-8451-ce1b691bd137.png)

El resultado es una matriz donde las dos primeras ranuras de cada fila contienen los valores más pequeños de esa fila, con los valores restantes rellenando las ranuras restantes.

# Datos estructurados: Arrays estructuradas de NumPy

Imagine que tenemos varias categorías de datos en un número de personas (por ejemplo, nombre, edad y peso), y nos gustaría almacenar estos valores para su uso en un programa Python. Sería posible almacenarlos en tres matrices separadas:

![image](https://user-images.githubusercontent.com/80594428/118006843-ff183000-b321-11eb-99a0-9c2a9bc48410.png)

![image](https://user-images.githubusercontent.com/80594428/118006862-02abb700-b322-11eb-83bb-e40f1040627e.png)

Aquí no hay nada que nos diga que las tres matrices están relacionadas; sería más natural si pudiéramos usar una sola estructura para almacenar todos estos datos. NumPy puede controlar esto a través de matrices estructuradas, que son matrices con tipos de datos compuestos.

Podemos crear una matriz estructurada utilizando una especificación de tipo de datos compuesto:

![image](https://user-images.githubusercontent.com/80594428/118007025-266efd00-b322-11eb-9527-8199dc1351f0.png)

Ahora que hemos creado una matriz de contenedores vacía, podemos llenar la matriz con nuestras listas de valores:

![image](https://user-images.githubusercontent.com/80594428/118007102-3686dc80-b322-11eb-9444-10362ec24ebb.png)

Con el enmascaramiento booleano, permite realizar algunas operaciones más sofisticadas, como filtrar a la edad:

![image](https://user-images.githubusercontent.com/80594428/118007138-3edf1780-b322-11eb-805e-c86d130f63dc.png)

![image](https://user-images.githubusercontent.com/80594428/118007155-443c6200-b322-11eb-9256-bf3c09bc7655.png)

