
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/que-son-las-tuplas-y-como-se-utilizan-en-python.webp)

## Introducción a las tuplas en Python

**Las tuplas son una estructura de datos en Python que te permiten almacenar una colección de valores ordenados y sin modificaciones.** A diferencia de una lista, las tuplas son inmutables, lo que significa que una vez que se crea una tupla, no se pueden agregar, eliminar o modificar elementos en ella. Las tuplas son muy útiles para almacenar datos que no necesitan ser modificados, como las coordenadas de un punto en un plano cartesiano.

En Python, las tuplas se crean colocando múltiples elementos entre paréntesis y separándolos con comas. Por ejemplo:

```py
mi_tupla = (1, 2, 3, 4)
```

También puedes crear una tupla vacía colocando solo paréntesis:

```py
tupla_vacia = ()
```

Al igual que con las listas, puedes acceder a los elementos individuales en una tupla utilizando su índice. Los índices en las tuplas comienzan en 0, lo que significa que el primer elemento tiene un índice de 0, el segundo elemento tiene un índice de 1 y así sucesivamente. Por ejemplo:

```py
mi_tupla = (1, 2, 3, 4)
print(mi_tupla[0])  # imprime 1
print(mi_tupla[1])  # imprime 2
```

También puedes usar la técnica de rebanado para acceder a una porción de una tupla. Por ejemplo:

```py
mi_tupla = (1, 2, 3, 4)
print(mi_tupla[1:3])  # imprime (2, 3)
```

Una de las ventajas de las tuplas es que son más eficientes en términos de memoria que las listas. Debido a que las tuplas son inmutables, Python no necesita reservar espacio adicional para futuras modificaciones en los elementos de la tupla.

Las tuplas también son útiles para devolver múltiples valores de una función. Por ejemplo, si tienes una función que calcula el perímetro y el área de un rectángulo, puedes usar una tupla para devolver ambos valores:

```py
def calcular_perimetro_y_area(base, altura):
    perimetro = 2 * (base + altura)
    area = base * altura
    return (perimetro, area)

resultado = calcular_perimetro_y_area(5, 10)
print(resultado)  # imprime (30, 50)
```

> [!TIP] TIP
> Las tuplas son una estructura de datos en Python que te permiten almacenar colecciones de valores ordenados y sin modificaciones. Las tuplas son inmutables, más eficientes en términos de memoria que las listas y son útiles para devolver múltiples valores de una función.

## Cómo declarar una tupla y sus características principales

Las **tuplas** son estructuras de datos en Python que permiten almacenar un conjunto de elementos de diferentes tipos en una única variable. Es decir, funcionan de manera similar a las listas, pero con la diferencia de que una vez que se ha creado una tupla, no puede ser modificada. Esta característica las hace muy útiles en situaciones en las que se requiere almacenar datos que no deben ser modificados, como por ejemplo las coordenadas de un punto en un plano cartesiano.

Para declarar una tupla en Python, se utiliza una sintaxis muy sencilla. Simplemente se delimita el conjunto de elementos por paréntesis y se separan los elementos por comas. Por ejemplo:

```py
mi_tupla = (10, "Hola", True, 3.14)
```

En este caso, estamos declarando una tupla llamada “mi_tupla” que contiene cuatro elementos de diferentes tipos: un entero, una cadena de texto, un booleano y un número decimal.

Una de las principales características de las tuplas es que, al igual que las listas, se pueden acceder a sus elementos mediante un índice. La diferencia es que **en las tuplas el índice empieza en cero y se accede al elemento con la sintaxis “tupla[indice]”**. Por ejemplo:

```py
mi_tupla = (10, "Hola", True, 3.14)

print(mi_tupla[0]) # Imprime 10
print(mi_tupla[1]) # Imprime "Hola"
print(mi_tupla[3]) # Imprime 3.14
```

Otra característica interesante de las tuplas es que **se pueden utilizar para asignar múltiples variables en una sola línea**. Esto se logra mediante la sintaxis “variable1, variable2, … = tupla”. Por ejemplo:

```py
mi_tupla = (10, "Hola", True, 3.14)

entero, texto, booleano, decimal = mi_tupla

print(entero) # Imprime 10
print(texto) # Imprime "Hola"
print(booleano) # Imprime True
print(decimal) # Imprime 3.14
```

Es importante mencionar que, al igual que las listas, **las tuplas también pueden contener tuplas anidadas**. Por ejemplo:

```py
tupla_anidada = ((1, 2), ("Hola", "Mundo"), (True, False))
```

> [!TIP] TIP
> Las tuplas son estructuras de datos muy útiles en Python que permiten almacenar un conjunto de elementos de diferentes tipos en una única variable. Se declaran utilizando paréntesis y se accede a sus elementos mediante un índice. Además, se pueden utilizar para asignar múltiples variables en una sola línea y pueden contener tuplas anidadas.

## Operaciones básicas con tuplas, como agregar y remover elementos

Las **tuplas** son objetos similares a las listas, pero a diferencia de estas, las tuplas son inmutables, lo que significa que una vez creadas sus elementos no pueden ser modificados. A pesar de esto, las tuplas siguen siendo muy útiles en la programación, especialmente en Python.

En esta sección, vamos a ver algunas operaciones básicas que podemos hacer con las tuplas, como agregar y remover elementos.

## Agregar elementos a una tupla

A diferencia de las listas, en las cuales podemos agregar elementos en cualquier momento, las tuplas son inmutables, por lo que no podemos agregar elementos directamente a una tupla existente. Sin embargo, podemos crear una nueva tupla que contenga los elementos de la tupla original más el nuevo elemento que queremos agregar.

Veamos un ejemplo:

```py
# Creamos una tupla con los números del 1 al 5
tupla_original = (1, 2, 3, 4, 5)

# Creamos una nueva tupla que contenga los elementos de la tupla original
# más un nuevo elemento
tupla_nueva = tupla_original + (6,)

# Imprimimos ambas tuplas para verificar que la nueva tenga el nuevo elemento
print(tupla_original)
print(tupla_nueva)
```

En este ejemplo, creamos una tupla llamada `tupla_original` que contiene los números del 1 al 5. Luego, creamos una nueva tupla llamada `tupla_nueva` que contiene los elementos de `tupla_original` más el número 6. Para hacer esto, simplemente usamos el operador `+` para concatenar ambas tuplas, y agregamos una coma después del 6 para indicar que estamos creando una tupla de un solo elemento.

## Remover elementos de una tupla

Como mencionamos al principio, las tuplas son inmutables, por lo que no podemos eliminar elementos directamente de una tupla existente. Sin embargo, podemos crear una nueva tupla que contenga solo los elementos que nos interesen.

Veamos un ejemplo:

```py
# Creamos una tupla con los números del 1 al 5
tupla_original = (1, 2, 3, 4, 5)

# Creamos una nueva tupla que contenga todos los elementos de la tupla original,
# excepto el primer elemento
tupla_nueva = tupla_original[1:]

# Imprimimos ambas tuplas para verificar que la nueva no tenga el primer elemento
print(tupla_original)
print(tupla_nueva)
```

En este ejemplo, creamos una tupla llamada `tupla_original` que contiene los números del 1 al 5. Luego, creamos una nueva tupla llamada `tupla_nueva` que contiene todos los elementos de `tupla_original`, excepto el primer elemento. Para hacer esto, usamos la sintaxis de rebanado (`[1:]`) para crear una nueva tupla que comienza en el segundo elemento de `tupla_original` y continúa hasta el final.

> [!TIP] TIP
> Aunque las tuplas son inmutables, aún podemos realizar varias operaciones básicas con ellas, como agregar y remover elementos. Si bien estos procesos no se realizan directamente en la tupla original, aún podemos crear nuevas tuplas que contengan los elementos que necesitamos. Con estas herramientas, podemos aprovechar al máximo el poder de las tuplas en Python.

## Diferencia entre tuplas y listas, y cómo elegir cuál utilizar

La elección entre usar una **lista** o una **tupla** puede parecer trivial, pero es importante comprender las diferencias y los beneficios de cada una. En general, una lista es una colección de elementos que se pueden modificar, agregar o eliminar, mientras que una tupla es una colección de elementos que no se pueden modificar una vez creadas.

Entonces, ¿por qué alguien elegiría una tupla sobre una lista? En muchas situaciones, las tuplas son más eficientes en términos de tiempo y memoria que las listas. Si tiene una gran cantidad de elementos que no necesitan cambiar, su programa funcionará mejor con una tupla que con una lista. Además, dado que las tuplas son inmutables, se pueden usar como claves de diccionario.

Un ejemplo de cuándo sería útil utilizar una tupla es si tiene coordenadas que no cambiarán, como las coordenadas de una ciudad conocida o un punto de referencia. Puede empaquetar estas coordenadas en una tupla y usarla como clave en un diccionario:

```py
coordenadas = (40.7128, -74.0060)
ciudades = {coordenadas: "Nueva York"}
```

Por otro lado, si desea agregar elementos a su colección o modificar elementos existentes, debe usar una lista. Las listas se pueden modificar en su longitud, lo que significa que puede agregar, eliminar o modificar elementos en cualquier momento. Por ejemplo, si desea llevar un registro de las ciudades en una lista, debe usar una lista:

```py
ciudades = ["Nueva York", "Los Ángeles", "Chicago"]
ciudades.append("San Francisco")
```

También es importante tener en cuenta que las tuplas se pueden utilizar en funciones para devolver múltiples valores de manera eficaz. En lugar de crear una lista para que la función devuelva múltiples valores, puede empaquetar esos valores en una tupla:

```py
def calcular_area_perimetro(rectangulo):
    altura = rectangulo[0]
    base = rectangulo[1]
    area = altura * base
    perimetro = 2 * (altura + base)
    return (area, perimetro)

rect = (4, 6)
area, perimetro = calcular_area_perimetro(rect)
```

> [!TIP] TIP
> La elección entre usar una tupla o una lista depende de si necesita una colección de elementos que pueda cambiar en el futuro. Si no necesita agregar, eliminar o modificar elementos en la colección, entonces una tupla puede ser más eficiente y efectiva. Si necesitas modificar elementos o agregar nuevos elementos, entonces una lista sería la opción correcta. En cualquier caso, asegúrese de comprender las diferencias entre las tuplas y las listas antes de elegir una para su proyecto.

## Cómo utilizar tuplas para retornar múltiples valores en una función

¿Alguna vez te has preguntado cómo retornar múltiples valores en una función en Python? Pues, las **tuplas** son la solución perfecta para este problema.

Una tupla es una estructura de datos que permite almacenar varios elementos de forma ordenada. Se utilizan para agrupar valores relacionados y pueden contener cualquier tipo de dato, incluso otras tuplas. Las tuplas se representan entre paréntesis y los elementos se separan por comas.

Aunque parezcan similares a las listas, las tuplas son diferentes en varios aspectos. La principal diferencia es que las tuplas son **inmutables**, lo que significa que una vez creadas, no se pueden modificar. Esto hace que sean más eficientes en términos de memoria y procesamiento que las listas.

Retornar múltiples valores en una función es muy simple usando tuplas. Supongamos que queremos escribir una función que calcule el área y el perímetro de un círculo dado su radio. Podemos hacerlo de la siguiente manera:

```py
def calcular_circulo(radio):
    pi = 3.14159
    area = pi * radio ** 2
    perimetro = 2 * pi * radio
    return (area, perimetro)
```

En esta función, estamos utilizando una tupla para retornar el área y el perímetro. En la última línea, estamos retornando una tupla que contiene dos elementos, el área y el perímetro.

Podemos utilizar esta función de la siguiente manera:

```py
>>> resultados = calcular_circulo(5)
>>> resultados
(78.53975, 31.4159)
>>> area, perimetro = resultados
>>> area
78.53975
>>> perimetro
31.4159
```

En primer lugar, llamamos a la función `calcular_circulo` con un radio de 5. La función retorna una tupla que contiene el área y el perímetro. Almacenamos esta tupla en la variable `resultados`.

Después, podemos acceder a cada elemento de la tupla usando la notación de índices o asignando la tupla a variables distintas.

Las tuplas también son útiles para iterar sobre múltiples valores en un bucle. Por ejemplo, si tenemos una lista de puntos en el plano cartesiano, donde cada punto es representado por una tupla de dos elementos (x, y), podemos iterar sobre los puntos de la siguiente manera:

```py
puntos = [(1, 2), (3, 4), (5, 6)]

for x, y in puntos:
    print(f"({x}, {y})")
```

En este caso, estamos utilizando la notación de asignación de tuplas para asignar los valores de x e y a cada elemento de la lista de puntos. Así, podemos imprimir los valores de cada punto de forma separada.

>[!TIP] TIP 
> Las tuplas son una herramienta poderosa y eficiente para trabajar con múltiples valores relacionados en Python. No solo son útiles para retornar múltiples valores en una función, sino que también nos permiten iterar sobre ellos de forma sencilla. Así que, la próxima vez que necesites almacenar varios elementos relacionados juntos, ¡prueba utilizar una tupla!

## Principales errores comunes al utilizar tuplas y cómo evitarlos

El uso de **tuplas** en Python es una forma conveniente de almacenar datos inmutables. Sin embargo, como con cualquier herramienta, hay algunos erroes comunes que se pueden cometer al utilizar tuplas.

Aquí mencionamos algunos de los errores más comunes y lo que se puede hacer para evitarlos:

### 1. Intentar modificar una tupla

Uno de los principales beneficios de las tuplas es que son inmutables. Esto significa que una vez que se crean, no se pueden modificar. Entonces, si intentamos agregar, eliminar o modificar elementos de una tupla, Python nos devolverá un error.

```py
tupla = (1, 2, 3)
tupla[0] = 2

TypeError: 'tuple' object does not support item assignment
```

Para evitar esto, simplemente asegúrate de que cualquier datos que necesiten ser modificados en el futuro se almacenen en otro tipo de objeto, como una **lista**.

### 2. Olvidarse de las comas al crear una tupla con un solo elemento

Al crear una tupla con un solo elemento, es fácil olvidarse de agregar una coma al final. Si esto sucede, Python lo tratará como un objeto que no es una tupla.

```py
tupla = (1)

TypeError: 'int' object is not iterable
```

Para solucionar este problema, asegúrate siempre de agregar una coma después del último elemento, incluso si solo hay un elemento.

### 3. Asignar el resultado de un cálculo a una tupla en lugar de una variable

Es común tener una expresión o una operación que devuelve varios valores. A veces, en lugar de almacenar estos valores en variables separadas, se asignan a una tupla.

```py
x = 5
y = 3

punto = (x + 2, y - 1)

# lo que intentabamos
(punto_x, punto_y) = (x + 2, y - 1)

# forma correcta
punto_x, punto_y = x + 2, y - 1
```

Cuando se intenta asignar los valores directamente a la tupla, Python utilizará la desempaquetación de tuplas y los valores se asignarán en un orden determinado. Si esto no se hace correctamente, podemos obtener errores difíciles de depurar.

### 4. Abusar de las tuplas anidadas

Es común tener tuplas anidadas, especialmente al trabajar con datos estructurados, como coordenadas o fechas. Sin embargo, no es una buena práctica abusar de las tuplas anidadas, ya que esto puede dificultar la lectura de código y complicar el mantenimiento.

Para evitar confusiones, utiliza tuplas individuales para cada valor o considera usar otro tipo de estructura de datos como un diccionario o un conjunto.

> [!TIP] TIP
> Conocer estos errores comunes y saber cómo evitarlos, te permitirá utilizar tuplas de manera efectiva y segura en tus proyectos de Python. Recuerda siempre seguir las mejores prácticas de programación y utilizar estas herramientas de la manera correcta para obtener resultados confiables y escalables.

