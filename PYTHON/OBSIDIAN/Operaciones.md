
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/conjuntos-en-python-operaciones-y-utilidades.webp)

Los **conjuntos** son una estructura de datos muy útil en Python que nos permiten guardar elementos únicos sin mantener un orden particular. Esto los convierte en una herramienta ideal para hacer comparaciones entre grupos de datos o para eliminar elementos duplicados de una lista. En esta sección, aprenderemos los conceptos esenciales que necesitamos saber para manejar conjuntos en Python.

Para comenzar, vamos a crear un conjunto y agregar algunos elementos. En Python, un conjunto se define utilizando llaves `{}` o utilizando la función `set()`.

```py
# Crear un conjunto
numeros = {1, 2, 3, 4, 5}
letras = set(['a', 'b', 'c', 'd'])
```

Los elementos dentro del conjunto deben ser inmutables, por lo que no podemos incluir listas, diccionarios ni otros conjuntos en su interior.

### Operaciones con conjuntos

Cuando tenemos dos conjuntos podemos realizar diferentes operaciones para compararlos o para unirlos. Algunas de las operaciones más comunes en Python son:

|**Operación**|**Descripción**|
|---|---|
|**Unión (`\|`)**|crea un nuevo conjunto con todos los elementos únicos de ambos conjuntos.|
|**Intersección (`&`)**|nos devuelve los elementos comunes entre dos conjuntos.|
|**Diferencia (`-`)**|nos devuelve los elementos presentes en el primer conjunto que no están en el segundo.|
|**Diferencia simétrica (`^`)**|nos devuelve los elementos únicos de ambos conjuntos que no están en el otro.|

```py
estudiantes_1 = {'Ana', 'Luis', 'Pedro', 'Sofía'}
estudiantes_2 = {'Fernando', 'Luis', 'Pedro', 'Sofía', 'Valeria'}

# Unión
todos_los_estudiantes = estudiantes_1 | estudiantes_2
print(todos_los_estudiantes) # {'Pedro', 'Fernando', 'Luis', 'Sofía', 'Valeria', 'Ana'}

# Intersección
estudiantes_repetidos = estudiantes_1 & estudiantes_2
print(estudiantes_repetidos) # {'Pedro', 'Luis', 'Sofía'}

# Diferencia
estudiantes_solo_grupo1 = estudiantes_1 - estudiantes_2
print(estudiantes_solo_grupo1) # {'Ana'}

# Diferencia simétrica
estudiantes_no_compartidos = estudiantes_1 ^ estudiantes_2
print(estudiantes_no_compartidos) # {'Ana', 'Fernando', 'Valeria'}
```

### Propiedades de los conjuntos

Los conjuntos tienen algunas propiedades muy interesantes que podemos utilizar. Una de ellas es la propiedad de que **solo puede existir un elemento de cada valor**. Esto significa que si tratamos de agregar un elemento que ya está dentro del conjunto, éste no se añadirá. Si queremos eliminar un elemento, podemos utilizar el método `remove()` o `discard()`.

```py
colores = {'rojo', 'naranja', 'amarillo', 'verde', 'azul'}

# Agregar un elemento
colores.add('violeta')
colores.add('rojo') # No se agrega, ya existe

# Eliminar un elemento
colores.remove('amarillo')
colores.discard('blanco') # No pasa nada, no existe

print(colores) # {'naranja', 'verde', 'rojo', 'azul', 'violeta'}
```

Otra propiedad que podemos mencionar es la capacidad de verificar si un conjunto es o no un subconjunto de otro. Para esto, podemos utilizar los métodos `issubset()` e `issuperset()`, respectivamente.

```py
numeros_pares = {2, 4, 6, 8, 10}
todos_los_numeros = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

# Verificar si es subconjunto
print(numeros_pares.issubset(todos_los_numeros)) # True

# Verificar si es superconjunto
print(todos_los_numeros.issuperset(numeros_pares)) # True
```

> [!TIP]
> Los conjuntos son una estructura de datos muy útil para manejar valores únicos y hacer comparaciones entre ellos. En Python, podemos utilizar diferentes operaciones para combinarlos y aprovechar algunas de sus propiedades para realizar tareas específicas. El manejo de conjuntos puede ser muy útil en situaciones en las que necesitamos comparar datos o reducir valores duplicados en una lista. ¡Anímate a experimentar con los conjuntos en Python!

## Operaciones básicas con conjuntos en Python

Los **conjuntos** son una estructura de datos muy útil en Python, ya que permiten almacenar colecciones de elementos únicos e inmutables. Además, los conjuntos admiten operaciones matemáticas, lo que los convierte en una herramienta poderosa en la programación.

A continuación, se describen las operaciones básicas que se pueden realizar con conjuntos en Python.

**Crear un conjunto:**

Para crear un conjunto, se pueden utilizar los corchetes {} o la función set().

```py
frutas = {"manzana", "naranja", "mango"}
colores = set(["rojo", "verde", "azul"])
```

**Agregar elementos a un conjunto:**

Para agregar un elemento a un conjunto, se utiliza la función add().

```py
frutas.add("piña")
```

**Eliminar elementos de un conjunto:**

Para eliminar un elemento de un conjunto, se utiliza la función remove().

```py
frutas.remove("mango")
```

**Unión de conjuntos:**

Para unir dos conjuntos, se utiliza el operador | o la función union().

```py
frutas_y_verduras = frutas | {"zanahoria", "lechuga"}
frutas_y_verduras = frutas.union(["zanahoria", "lechuga"])
```

**Intersección de conjuntos:**

Para obtener los elementos que dos conjuntos tienen en común, se utiliza el operador & o la función intersection().

```py
sabores = {"dulce", "salado", "picante"}
postres = {"dulce", "amargo", "ácido"}
dulces = sabores & postres
dulces = sabores.intersection(postres)
```

**Diferencia de conjuntos:**

Para obtener los elementos que están en un conjunto pero no en otro, se utiliza el operador - o la función difference().

```py
números = {1, 2, 3, 4, 5}
pares = {2, 4, 6}
impares = números - pares
impares = números.difference(pares)
```

**Subconjunto y superconjunto:**

Para saber si un conjunto es un subconjunto de otro, se utiliza el operador <= o la función issubset(). Para saber si un conjunto es un superconjunto de otro, se utiliza el operador >= o la función issuperset().

```py
días_laborables = {"lunes", "martes", "miércoles", "jueves", "viernes"}
días_del_mes = {"1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12", "13", "14", "15", "16", "17", "18", "19", "20", "21", "22", "23", "24", "25", "26", "27", "28", "29", "30", "31"}
laborables_de_junio = días_laborables.issubset(días_del_mes)
todos_los_días = días_del_mes.issuperset(días_laborables)
```

> [!TIP]
> Los conjuntos permiten realizar operaciones matemáticas de una manera sencilla y eficiente. Además, dado que los elementos son únicos e inmutables, son muy adecuados para manejar colecciones de datos que deben ser procesadas de manera eficiente en una aplicación.

## Utilidades avanzadas para conjuntos en Python

Los conjuntos en Python son una estructura de datos fundamental que se utiliza para almacenar elementos únicos sin repetición. Ya hemos hablado de las operaciones básicas de los conjuntos en Python, como la intersección, unión, diferencia y diferencia simétrica. En este artículo, profundizaremos en algunas utilidades avanzadas para los conjuntos en Python.

## Subconjuntos y superconjuntos

Los subconjuntos y superconjuntos de un conjunto son dos conceptos importantes que debemos conocer. Decimos que un conjunto A es un subconjunto de otro conjunto B si cada elemento de A también está en B. La notación para esto es A ⊆ B, y si alguno de los elementos de A no se encuentra en B, entonces decimos que A no es subconjunto de B. En Python, podemos comprobar si un conjunto es subconjunto de otro usando el método `issubset()`.

```python
A = {1,2,3}
B = {1,2,3,4,5}
print(A.issubset(B)) # True
```

Por otro lado, decimos que un conjunto A es un superconjunto de otro conjunto B si cada elemento de B también está en A. La notación para esto es A ⊇ B, y de forma similar a los subconjuntos, podemos comprobar esto en Python usando `issuperset()`.

```python
A = {1,2,3,4}
B = {1,2,3}
print(A.issuperset(B)) # True
```

## Conjuntos como filtros

En muchas ocasiones, podemos utilizar conjuntos para filtrar listas. Por ejemplo, supongamos que tenemos una lista de números y queremos quedarnos solo con los que son divisibles entre 3. Podemos generar un conjunto que contenga todos los números que son múltiplos de 3 y luego filtrar nuestra lista de acuerdo a este conjunto.

```python
numeros = [1,2,3,4,5,6,7,8,9,10]
multiplos_3 = {n for n in numeros if n % 3 == 0} # generamos el conjunto de múltiplos de 3
numeros_filtrados = [n for n in numeros if n in multiplos_3] # filtramos la lista usando el conjunto de múltiplos de 3
print(numeros_filtrados) # [3, 6, 9]
```

De esta forma, podemos utilizar conjuntos como filtros avanzados para manipular fácilmente grandes cantidades de datos.

## Conjuntos inmutables

Hasta ahora, hemos trabajado con conjuntos mutables. Esto significa que podemos modificar el contenido del conjunto mediante la adición o eliminación de elementos. Sin embargo, en ocasiones es útil tener conjuntos inmutables, que son conjuntos que no pueden ser modificados después de su creación.

En Python, podemos crear conjuntos inmutables utilizando el tipo de datos `frozenset()`. Los conjuntos inmutables a menudo se utilizan en combinación con conjuntos mutables para asegurarse de que los elementos originales de un conjunto no se modifiquen accidentalmente.

```python
conjunto = {1,2,3}
conjunto_inmutable = frozenset(conjunto) # creamos el conjunto inmutable a partir del conjunto original
print(conjunto_inmutable) # frozenset({1, 2, 3})
```

>[!TIP]
> Los conjuntos en Python son una herramienta muy útil para el procesamiento de datos y el análisis de datos. En este artículo, hemos visto algunas utilidades avanzadas de los conjuntos en Python, como el uso de subconjuntos y superconjuntos, conjuntos como filtros, y conjuntos inmutables. Con estas herramientas, podemos manipular fácilmente grandes conjuntos de datos y obtener información valiosa.

## Intersección, unión y diferencia simétrica de conjuntos en Python

Si hay algo que me gusta de Python son sus operaciones con conjuntos. Cuando empecé a programar, no sabía que estas operaciones existían, pero a medida que fui explorando el lenguaje, descubrí lo útiles que son para simplificar el código y hacer las cosas más eficientemente.

Las operaciones que más me gusta utilizar son la intersección, unión y diferencia simétrica de conjuntos. Con ellas, puedo calcular rápidamente la relación entre dos o más conjuntos y obtener los resultados que necesito en mis programas.

La **intersección** de conjuntos es la operación que se encarga de encontrar los elementos que se encuentran en ambos conjuntos. En Python, se puede utilizar el operador “&” o la función “intersection” para realizar esta operación. Por ejemplo:

```python
A = {1, 2, 3, 4, 5}
B = {3, 4, 5, 6, 7}
C = A & B  # Esta es la intersección de A y B utilizando el operador "&"
D = A.intersection(B)  # Esta es la intersección de A y B utilizando la función "intersection"
print(C)  # Output: {3, 4, 5}
print(D)  # Output: {3, 4, 5}
```

La **unión** de conjuntos, por otro lado, se encarga de encontrar todos los elementos de ambos conjuntos sin repetir ninguno. Para realizar esta operación, se puede utilizar el operador “|” o la función “union”. Por ejemplo:

```python
A = {1, 2, 3, 4, 5}
B = {3, 4, 5, 6, 7}
C = A | B  # Esta es la unión de A y B utilizando el operador "|"
D = A.union(B)  # Esta es la unión de A y B utilizando la función "union"
print(C)  # Output: {1, 2, 3, 4, 5, 6, 7}
print(D)  # Output: {1, 2, 3, 4, 5, 6, 7}
```

Por último, la **diferencia simétrica** de conjuntos se encarga de encontrar los elementos que se encuentran en uno de los conjuntos pero no en ambos. Para realizar esta operación, se puede utilizar el operador “^” o la función “symmetric_difference”. Por ejemplo:

```python
A = {1, 2, 3, 4, 5}
B = {3, 4, 5, 6, 7}
C = A ^ B  # Esta es la diferencia simétrica de A y B utilizando el operador "^"
D = A.symmetric_difference(B)  # Esta es la diferencia simétrica de A y B utilizando la función "symmetric_difference"
print(C)  # Output: {1, 2, 6, 7}
print(D)  # Output: {1, 2, 6, 7}
```

Estas operaciones son muy útiles en la programación, ya que permiten trabajar con conjuntos de manera eficiente y sencilla. Personalmente, las utilizo cuando tengo que comparar datos o hacer cálculos que involucren varias listas o conjuntos de elementos.

> [!TIP]
> La intersección, unión y diferencia simétrica de conjuntos son operaciones imprescindibles en Python. Con ellas, podemos simplificar nuestro código y hacer nuestras tareas de programación más eficientes y fáciles de realizar.

## Operaciones avanzadas con conjuntos en Python

Los **conjuntos** en Python son una estructura de datos que nos permite almacenar elementos únicos. Además de operaciones básicas como la creación de conjuntos o la adición y eliminación de elementos, existen una serie de operaciones avanzadas que podemos realizar con conjuntos en Python. A continuación, te contamos de algunas de ellas.

#### 1. Unión, intersección y diferencia de conjuntos

Una de las operaciones más útiles en conjuntos es la **unión**. La unión de dos conjuntos es un nuevo conjunto que contiene todos los elementos de ambos conjuntos:

```python
a = {1, 2, 3}
b = {3, 4, 5}
c = a.union(b)
print(c)  # {1, 2, 3, 4, 5}
```

Por otro lado, la **intersección** de dos conjuntos es un nuevo conjunto que contiene solo los elementos que aparecen en ambos conjuntos:

```python
a = {1, 2, 3}
b = {3, 4, 5}
c = a.intersection(b)
print(c)  # {3}
```

La **diferencia** de dos conjuntos es un nuevo conjunto que contiene los elementos que aparecen en uno de los conjuntos pero no en el otro:

```python
a = {1, 2, 3}
b = {3, 4, 5}
c = a.difference(b)
print(c)  # {1, 2}
```

#### 2. Comprobar si un conjunto es un subconjunto de otro

Otra operación muy útil en conjuntos es comprobar si un conjunto es un **subconjunto** de otro. Para ello, podemos utilizar el método `issubset()`:

```python
a = {1, 2, 3}
b = {1, 2}
c = {4, 5}
print(b.issubset(a))  # True
print(c.issubset(a))  # False
```

También podemos comprobar si un conjunto es un **superconjunto** de otro utilizando el método `issuperset()`.

#### 3. Eliminar elementos duplicados de una lista

En ocasiones, podemos tener una lista con elementos duplicados y queremos eliminarlos. Una forma sencilla de hacerlo es convertir la lista a un conjunto y luego volver a convertirlo a una lista. De esta forma, se eliminan automáticamente los elementos duplicados:

```python
a = [1, 2, 3, 2, 4, 1]
b = list(set(a))
print(b)  # [1, 2, 3, 4]
```

#### 4. Conjuntos con elementos inmutables

En Python, los elementos de un conjunto deben ser inmutables, es decir, no pueden ser modificados una vez que se han insertado en el conjunto. Esto se debe a que los conjuntos utilizan una tabla hash para almacenar los elementos y si un elemento se pudiera modificar, su posición en la tabla también tendría que modificarse, lo que sería ineficiente.

> [!TIP]
> Los conjuntos en Python nos permiten realizar una serie de operaciones avanzadas como la unión, intersección y diferencia de conjuntos, comprobar si un conjunto es un subconjunto de otro, eliminar elementos duplicados de una lista y trabajar con elementos inmutables. Estas operaciones son muy útiles en distintos escenarios y nos ayudan a trabajar de forma más eficiente con conjuntos en Python.

