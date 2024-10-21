![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/que-son-las-listas-y-como-se-utilizan-en-python.webp)

## En este artículo se explicará qué son y cómo se usan las listas en Python

Si estás interesado en aprender programación, seguramente habrás escuchado hablar de las **listas en Python**. Pero, ¿realmente sabes qué son y cómo se utilizan?

En términos sencillos, una lista es una colección ordenada de elementos que pueden ser de cualquier tipo. Esto significa que puedes crear una lista de números, palabras, objetos, funciones, etc.

Las listas en Python se definen entre corchetes, y los elementos se separan por comas. Por ejemplo, para crear una lista de números, puedes hacer lo siguiente:

```python
numeros = [1, 2, 3, 4, 5]
```

Una vez que has creado la lista, puedes acceder a sus elementos mediante su índice. El índice es la posición del elemento en la lista, y comienza en cero. Por ejemplo, para acceder al segundo elemento de una lista, puedes hacer lo siguiente:

```python
numeros = [1, 2, 3, 4, 5]
segundo_numero = numeros[1]
```

En este caso, `segundo_numero` tendría el valor de `2`.

Otra operación común que puedes hacer con las listas es agregar nuevos elementos. Para ello, puedes utilizar el método `append()`. Por ejemplo, si quisieras agregar el número `6` a la lista de `numeros`, puedes hacer lo siguiente:

```python
numeros.append(6)
```

También puedes modificar elementos en una lista mediante su índice. Por ejemplo, si quisieras cambiar el valor del tercer elemento de la lista `numeros` a `10`, puedes hacer lo siguiente:

```python
numeros[2] = 10
```

Por último, las listas en Python también cuentan con una variedad de métodos útiles, como `sort()` para ordenar los elementos de la lista, o `reverse()` para invertir el orden de los elementos.

> [!TIP] TIP
> Las listas en Python son una herramienta poderosa y versátil que te permiten almacenar y trabajar con colecciones de elementos de distintos tipos. Si estás comenzando en el mundo de la programación, es fundamental que aprendas a utilizarlas adecuadamente para aprovechar todo su potencial.

## Las listas son una colección ordenada y mutable de elementos

Las **listas** son una de las estructuras de datos más utilizadas en el lenguaje de programación Python. En pocas palabras, una lista es una colección ordenada y mutable de elementos que puede contener cualquier tipo de datos, ya sea números, texto, objetos, entre otros.

Si eres nuevo en Python, quizás te preguntes **¿Qué significa exactamente mutable?** Pues bien, en este contexto, mutable quiere decir que las listas pueden ser modificadas: puedes agregar, eliminar o modificar elementos en una lista después de que ha sido creada.

Para crear una lista en Python, simplemente debes utilizar corchetes [ ] y separar los elementos con comas. Por ejemplo, para crear una lista que contenga los números del 1 al 5, puedes ejecutar el siguiente código:

```python
numeros = [1, 2, 3, 4, 5]
```

Una vez que tienes una lista creada, puedes acceder a sus elementos utilizando índices. En Python, al igual que en otros lenguajes de programación, los índices comienzan en 0. Por ejemplo, para acceder al primer elemento de la lista creada anteriormente, puedes ejecutar el siguiente código:

```python
primer_numero = numeros[0]
```

De igual forma, puedes acceder a los otros elementos de la lista utilizando índices, como se muestra en el siguiente ejemplo:

```python
segundo_numero = numeros[1]
tercer_numero = numeros[2]
cuarto_numero = numeros[3]
quinto_numero = numeros[4]
```

Además, como mencionamos anteriormente, las listas son **mutables**, por lo que puedes agregar o eliminar elementos de una lista en cualquier momento. Para agregar un elemento al final de una lista, puedes utilizar el método append(). Por ejemplo, si deseas agregar el número 6 a la lista de números que creamos anteriormente, puedes ejecutar el siguiente código:

```python
numeros.append(6)
```

Asimismo, para eliminar un elemento de una lista, puedes utilizar el método remove(). Supongamos que quieres eliminar el número 3 de la lista de números, puedes hacerlo de la siguiente manera:

```python
numeros.remove(3)
```

Otra forma de modificar una lista es mediante la reasignación de un elemento en particular. Por ejemplo, si deseas cambiar el valor del segundo elemento en la lista de números a 10, puedes hacerlo de la siguiente manera:

```python
numeros[1] = 10
```

En resumen, las listas son una estructura fundamental en Python que nos permite almacenar y manipular colecciones de elementos. Como hemos visto, son muy útiles ya que son ordenadas, mutables y pueden contener cualquier tipo de datos. Además, Python ofrece una gran cantidad de métodos y operaciones que nos permiten trabajar con las listas de manera muy eficiente.

> [!TIP]
> Si bien existen otros tipos de estructuras de datos en Python, como las tuplas y los conjuntos, las listas son una herramienta fundamental para cualquier programador que trabaje con este lenguaje. Espero que este artículo te haya ayudado a entender un poco mejor qué son las listas y cómo se utilizan en Python.

## Se pueden agregar, eliminar o iterar elementos en una lista

En Python, una **lista** es una estructura de datos que nos permite almacenar y acceder a varios valores en un solo lugar. Imagina que tienes varios nombres que quieres guardar, en lugar de crear variables separadas para cada nombre, puedes crear una lista y agregar cada nombre a la lista.

Una de las ventajas de las listas es que se pueden agregar, eliminar o iterar elementos fácilmente. Por ejemplo, si quieres agregar un nombre nuevo a la lista, solo necesitas usar la función **append()**. Aquí te muestro un ejemplo:

```python
nombres = ["Ana", "Pedro", "Sofía"]
nombres.append("Juan")
```

Ahora la lista `nombres` tiene los valores `["Ana", "Pedro", "Sofía", "Juan"]`. Como puedes ver, la función `append()` agrega el nuevo elemento al final de la lista.

Si por algún motivo quieres eliminar un elemento de la lista, puedes usar la función **remove()**. Por ejemplo, si quieres eliminar al nombre “Pedro” de la lista, puedes hacer lo siguiente:

```python
nombres.remove("Pedro")
```

Ahora la lista `nombres` tiene los valores `["Ana", "Sofía", "Juan"]`. La función `remove()` elimina el primer elemento que coincide con el valor que le pasamos como argumento, en este caso el valor “Pedro”.

También podemos iterar por cada elemento en la lista usando un **bucle for**. Por ejemplo, si queremos imprimir cada nombre en la lista, podemos hacer lo siguiente:

```python
for nombre in nombres:
  print(nombre)
```

Este código imprimirá lo siguiente:

```txt
Ana
Sofía
Juan
```

Como puedes ver, el bucle for itera por cada elemento en la lista `nombres` y lo imprime.

Además de agregar y eliminar elementos, también podemos acceder a ellos individualmente usando **índices**. En Python (y en muchos otros lenguajes de programación), los índices comienzan en 0. Por lo tanto, si queremos acceder al primer elemento en la lista `nombres`, podemos hacerlo así:

```python
primer_nombre = nombres[0]
```

Esto asignará el valor “Ana” a la variable `primer_nombre`. Si quieres acceder al segundo o tercer elemento, puedes usar los índices 1 y 2 respectivamente.

> [!TIP]
> Las listas en Python son una herramienta muy útil para almacenar y acceder a varios valores. Se pueden agregar, eliminar o iterar elementos fácilmente, y también podemos acceder a ellos individualmente usando índices. Estos son solo algunos de los conceptos básicos de las listas en Python, ¡sigue explorando y descubre todo lo que puedes hacer con ellas!

## Las listas pueden contener elementos de diferentes tipos, incluyendo otras listas

Las **listas** son uno de los elementos más útiles e importantes en Python. Estas son creadas utilizando corchetes `[]` y pueden contener cualquier tipo de elemento, incluyendo otros objetos del mismo tipo o incluso otras listas.

Personalmente, las listas me han permitido crear programas más eficientes y flexibles al permitirme almacenar y manipular grandes cantidades de datos de manera organizada.

Un ejemplo de una lista que contiene diferentes tipos de elementos podría ser:

```python
    lista_ejemplo = [1, "dos", True, [4, 5, 6]]
```

En este caso, la lista tiene un entero, una cadena de texto, un booleano y otra lista como elementos.

Para acceder a los elementos dentro de una lista, se utiliza la sintaxis de índices. Los índices en Python comienzan en 0, lo que significa que el primer elemento de una lista estaría en la posición 0. Para acceder a un elemento específico en la lista, se puede utilizar su índice en los corchetes después del nombre de la lista.

Por ejemplo, para acceder al segundo elemento en la lista de `lista_ejemplo`, se podría hacer lo siguiente:

```python
    segundo_elemento = lista_ejemplo[1]
```

Esto asignaría `"dos"`, que es el segundo elemento en la lista, a la variable `segundo_elemento`.

Además de acceder a elementos individuales, también se pueden realizar operaciones en toda la lista. Por ejemplo, se puede encontrar la longitud de una lista utilizando la función incorporada `len()`:

```python
    longitud_lista = len(lista_ejemplo)
```

Esto asignaría el valor `4` a la variable `longitud_lista`.

También es posible modificar elementos individuales en la lista o agregar nuevos elementos al final utilizando el operador de asignación (`=`) y la función `append()`:

```python
    lista_ejemplo[1] = "tres"
    lista_ejemplo.append(7)
```

Esto cambiaría el segundo elemento de la lista a `"tres"` y agregaría un entero `7` al final de la lista.

Otro ejemplo práctico de cómo usar una lista que contenga listas podría ser utilizar una lista para almacenar datos de una clase en una escuela. Por ejemplo:

```python
    clase = [
        ["Juan", 15, "A"],
        ["María", 16, "B"],
        ["Pedro", 15, "A"],
        ["Luisa", 17, "C"]
    ]
```

En este ejemplo, cada elemento de la lista es una lista que contiene el nombre, la edad y la sección de un estudiante en particular. Cada elemento de esta lista interna se puede acceder utilizando índices dentro de la lista general.

> [!TIP]
> Las listas pueden ser muy potentes y flexibles en Python, especialmente cuando se combinan con otras características del lenguaje como bucles y condicionales. Al aprender a trabajar con listas, los programadores pueden realizar muchas tareas en menos líneas de código.

## Las listas son una herramienta poderosa en la programación, útiles en una amplia gama de aplicaciones

En nuestro viaje como programadores, las listas son una herramienta que nos acompañará en muchas aventuras. Son una estructura de datos flexible y dinámica, que podemos utilizar de muchas maneras diferentes. Con las listas, podemos almacenar y manipular muchos elementos de datos diferentes, desde números y strings hasta objetos más complejos.

En Python, podemos crear una lista simplemente colocando elementos entre corchetes `[]` y separándolos por comas `,`. Por ejemplo, aquí hay una lista simple de nombres de frutas:

```python
frutas = ['manzana', 'naranja', 'pera', 'plátano']
```

Podemos acceder a los elementos individuales de una lista usando su índice numérico. El primer elemento de la lista tiene el índice `0`, el segundo elemento tiene el índice `1`, y así sucesivamente. Podemos acceder a los elementos de la lista utilizando corchetes `[]` y el índice de la posición que queremos:

```python
frutas = ['manzana', 'naranja', 'pera', 'plátano']
print(frutas[0])  # 'manzana'
print(frutas[2])  # 'pera'
```

Podemos agregar elementos a una lista utilizando el método `append()`, que agrega elementos al final de la lista:

```python
frutas = ['manzana', 'naranja', 'pera', 'plátano']
frutas.append('fresa')
print(frutas)  # ['manzana', 'naranja', 'pera', 'plátano', 'fresa']
```

Podemos eliminar elementos de una lista utilizando las palabras clave `del` o `remove()`. La palabra clave `del` elimina un elemento en una posición específica, mientras que el método `remove()` elimina un elemento específico por su valor:

```python
frutas = ['manzana', 'naranja', 'pera', 'plátano']
del frutas[0]  # elimina 'manzana'
print(frutas)  # ['naranja', 'pera', 'plátano']
frutas.remove('pera')
print(frutas)  # ['naranja', 'plátano']
```

Las listas pueden contener una mezcla de diferentes tipos de elementos, incluyendo otras listas. Esto significa que podemos crear estructuras de datos más complejas y jerárquicas con listas anidadas:

```python
lista_anidada = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(lista_anidada[1][2])  # 6
```

También podemos utilizar ciclos para recorrer los elementos de una lista para realizar operaciones en ellos:

```python
frutas = ['manzana', 'naranja', 'pera', 'plátano']
for fruta in frutas:
    print(f'Me gusta comer {fruta}s')
```

> [!TIP] 
> Las listas son flexibles, dinámicas y útiles en una amplia gama de aplicaciones. Ya sea que estemos almacenando una lista simple de valores o estructurando datos más complejos, las listas son una herramienta valiosa que podemos utilizar en nuestro arsenal de programación.

