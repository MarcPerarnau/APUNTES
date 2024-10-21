
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/manejo-de-argumentos-en-funciones-python-flexibilidad-y-adaptabilidad.webp)

## Introducción al manejo de argumentos en funciones Python

El **manejo de argumentos en funciones Python** es un concepto fundamental que cualquier desarrollador debe conocer para aprovechar al máximo este lenguaje de programación.

Los argumentos en funciones se refieren a los valores que se pasan a una función para que realice una tarea específica. Como desarrolladores, es común encontrarnos con situaciones en las que necesitamos que una función tome distintos valores para realizar una tarea en particular.

La **flexibilidad y adaptabilidad** que ofrecen las funciones Python en el manejo de argumentos es una característica única en el lenguaje, lo que lo convierte en una herramienta poderosa para el desarrollo de aplicaciones complejas.

Existen diferentes tipos de argumentos que se pueden pasar a una función en Python:

## Argumentos posicionales

Este tipo de argumentos se pasan a una función en el orden en que se definieron en la firma de la función. Por ejemplo:

```py
def suma(a, b):
    return a + b

result = suma(2, 3)
print(result) # Imprime 5
```

En este ejemplo, los argumentos `a` y `b` son argumentos posicionales y se pasan en el orden en que se definieron en la firma de la función `suma`.

## Argumentos con valor por defecto

Los argumentos con valor por defecto son aquellos que se les asigna un valor en la firma de la función, pero también se pueden sobrescribir en tiempo de ejecución.

```py
def multiplicacion(a, b=2):
    return a * b

result1 = multiplicacion(3) # Imprime 6
result2 = multiplicacion(3, 5) # Imprime 15
```

En este ejemplo, el argumento `b` tiene un valor por defecto de `2`, pero también se puede sobrescribir en tiempo de ejecución.

## Argumentos con nombre

Los argumentos con nombre se pasan a una función especificando su nombre en la llamada a la función. Este tipo de argumentos proporcionan una mayor claridad y legibilidad al código.

```py
def resta(a, b):
    return a - b

result = resta(b=3, a=5)
print(result) # Imprime 2
```

En este ejemplo, los argumentos `a` y `b` se pasan con nombre y no en el orden en que se definieron en la firma de la función `resta`.

>  
> 
> El manejo de argumentos en funciones Python es una técnica fundamental que cualquier desarrollador debe conocer. En Python, la flexibilidad y adaptabilidad que ofrecen las funciones en el manejo de argumentos lo convierten en un lenguaje de programación poderoso para el desarrollo de aplicaciones complejas.

## Cómo utilizar argumentos posicionales en Python

Uno de los aspectos más importantes del [manejo de argumentos en funciones Python](https://www.python.org/dev/peps/pep-3102/) es la posibilidad de utilizar argumentos posicionales. ¿Qué son los argumentos posicionales? Son los argumentos que se envían a una función en el orden en que se definieron, es decir, el primer argumento será el primero que se envíe, el segundo será el segundo, y así sucesivamente.

Utilizar **argumentos posicionales** puede ser muy útil cuando se requiere una flexibilidad de argumentos, ya que, al enviar los argumentos en orden, no es necesario preocuparse por escribir la lista completa de argumentos y sus valores en la llamada a la función.

Veamos un ejemplo:

```py
def resta(a, b):
    return a - b

resta(6, 4)
```

En este caso, la función `resta` toma dos argumentos posicionales `a` y `b`, por lo que, en la llamada a la función, se enviarán los valores de `a` y `b` en ese orden.

En nuestro ejemplo, al llamar a la función con `resta(6, 4)`, se está enviando `a=6` y `b=4`, por lo que el resultado será `2`.

Otro ejemplo usando una función para imprimir información de una persona:

```py
def informacion_persona(nombre, edad, ciudad):
    print(f"{nombre} tiene {edad} años y vive en {ciudad}")

informacion_persona("Juan", 25, "Madrid")
```

La función `informacion_persona` recibe tres argumentos posicionales, `nombre`, `edad` y `ciudad`. Al llamar a la función con `informacion_persona("Juan", 25, "Madrid")`, se enviaron los valores `nombre="Juan"`, `edad=25` y `ciudad="Madrid"`, por lo que la función imprimirá `Juan tiene 25 años y vive en Madrid`.

Es importante notar que, aunque el orden en que se envían los argumentos es importante en las funciones con argumentos posicionales, también es posible definir valores por defecto para los argumentos en caso de no ser específicados en la llamada a la función.

```py
def informacion_persona(nombre, edad=18, ciudad="Desconocida"):
    print(f"{nombre} tiene {edad} años y vive en {ciudad}")

informacion_persona("María")
```

En este ejemplo, se define un valor por defecto de `edad=18` y `ciudad="Desconocida"`. Al llamar a la función con `informacion_persona("María")`, se envía el valor de `nombre="María"`, pero no se envía ningún valor para `edad` ni `ciudad`, por lo que se utilizarán los valores por defecto definidos en la función. El resultado impreso por la función sería `María tiene 18 años y vive en Desconocida`.

>  
> 
> El uso de argumentos posicionales en Python brinda flexibilidad a las funciones al permitir una llamada más simple y ordenada para una variedad de argumentos. Además, se pueden definir valores por defecto para los argumentos en caso de no ser enviados en la llamada a la función.

## Cómo utilizar argumentos con palabras clave en Python

Cuando programamos en Python, no solo debemos preocuparnos por la lógica de nuestro código, sino también por su **flexibilidad y adaptabilidad**. Una de las formas en las que podemos lograr esto es mediante el uso de argumentos con palabras clave.

Antes de profundizar en el tema, es importante conocer la definición de los argumentos con palabras clave. Estos son aquellos que se definen mediante una palabra clave seguida de un signo igual y su valor correspondiente. Por ejemplo, en una función que recibe los argumentos `nombre` y `edad`, podríamos utilizar la siguiente sintaxis para llamar a la función:

```py
mi_funcion(nombre="Juan", edad=25)
```

De esta forma, Python sabe con exactitud qué valor le corresponde a cada argumento, lo que puede resultar muy útil en casos donde nuestra función recibe muchos argumentos o cuando queremos hacer nuestro código más legible.

Ahora bien, ¿cómo podemos utilizar argumentos con palabras clave en Python? La respuesta es sencilla: basta con declarar los argumentos de nuestra función de la forma `argumento=valor`. Veamos un ejemplo sencillo:

```py
def suma_numeros(num1, num2, mostrar_resultado=False):
    resultado = num1 + num2
    if mostrar_resultado:
        print("El resultado de la suma es:", resultado)
    return resultado
```

En este caso, nuestra función `suma_numeros` recibe dos números como argumentos (`num1` y `num2`) y un parámetro opcional `mostrar_resultado`. Si no definimos este último parámetro, su valor por defecto será `False`. Si seteamos este parámetro a `True`, la función imprimirá en pantalla el resultado. Podemos llamar a esta función de la siguiente forma:

```py
resultado = suma_numeros(3, 4)
# resultado es 7
resultado = suma_numeros(3, 4, mostrar_resultado=True)
# imprime "El resultado de la suma es: 7" y asigna 7 a resultado
```

Como podemos ver, gracias a la utilización de argumentos con palabras clave, podemos hacer que nuestra función sea más flexible y adaptable a diferentes casos de uso.

>  
> 
> Los argumentos con palabras clave son una herramienta muy útil en Python para hacer nuestro código más legible y adaptable. Para utilizarlos en nuestras funciones, basta con definir los argumentos de la forma `argumento=valor`. Con esta técnica, podemos hacer que nuestras funciones se adapten a diferentes situaciones sin tener que cambiar su lógica interna.

## Cómo utilizar argumentos por defecto en Python

En Python, los argumentos en las funciones pueden ser manejados de manera flexible y adaptable para adaptarse a diferentes casos de uso. Una forma en que podemos hacer esto es mediante el uso de argumentos por defecto.

Los argumentos por defecto son valores que se asignan a los parámetros de una función en caso de que no se proporcionen valores para ellos al llamar a la función. Esto puede ser útil para proporcionar un valor predeterminado que la función puede usar si no se proporciona un valor específico.

Para utilizar argumentos por defecto en Python, se puede proporcionar un valor predeterminado al definir los parámetros de una función. Por ejemplo, consideremos la siguiente función que toma dos argumentos y los concatena:

```py
def concatenar(a, b):
    return a + b
```

Si no se proporciona algún valor para los argumentos `a` y `b` al llamar a la función, se producirá un error. Para evitar esto, podemos proporcionar valores por defecto para `a` y `b`. Por ejemplo:

```py
def concatenar(a="", b=""):
    return a + b
```

En este ejemplo, se proporcionan dos valores por defecto para `a` y `b`. Si no se proporciona un valor para `a` o `b` al llamar a la función, se utilizarán estos valores predeterminados.

Es importante tener en cuenta que los valores por defecto solo se evalúan una vez, al definir la función. Esto significa que si se usa un objeto mutable (por ejemplo, una lista o un diccionario) como valor por defecto, se pueden producir resultados inesperados. En el siguiente ejemplo, se usará una lista como valor predeterminado para el parámetro `lista`:

```py
def agregar_elemento(elemento, lista=[]):
    lista.append(elemento)
    return lista
```

Al llamar a esta función sin proporcionar una lista, se utilizará la lista predeterminada:

```py
print(agregar_elemento(1))	#imprimirá [1]
```

Si llamamos a la función de nuevo con un objeto diferente, veremos que ambas llamadas a la función están añadiendo el elemento a la misma lista:

```py
print(agregar_elemento(2))	#imprimirá [1, 2]
```

Para evitar este comportamiento inesperado, podemos utilizar un valor por defecto que no sea un objeto mutable. Por ejemplo, podemos usar None y luego dentro de la función creamos la lista o cualquier objeto que deseemos usar.

```py
def agregar_elemento(elemento, lista=None):
    if lista is None:
        lista = []
    lista.append(elemento)
    return lista
```

>  
> 
> El uso de argumentos por defecto puede ayudar a hacer que nuestras funciones sean más flexibles y adaptativas a diferentes casos de uso. Al proporcionar valores predeterminados para los parámetros, podemos evitar errores y mejorar la usabilidad de nuestras funciones.

## Cómo utilizar argumentos variables en Python

En Python, uno de los aspectos más importantes a la hora de definir funciones es la gestión de argumentos y parámetros. Una herramienta fundamental son los argumentos variables, que permiten trabajar con un número indeterminado de elementos que se pasan como argumentos a una función.

Los argumentos variables en Python se definen con el operador `*` para las listas y tuplas, o con `**` para los diccionarios. De esta manera, cuando se utiliza la función con estos argumentos variables se pueden pasar tantos elementos como se quiera. Por ejemplo, supongamos que deseamos definir una función que calcule el promedio de un conjunto de números. Eine forma de hacerlo es mediante una función que reciba una lista de elementos como argumento:

```py
def promedio(num):
    return sum(num) / len(num)

print(promedio([1, 2, 3, 4])) # output: 2.5
```

Sin embargo, si queremos calcular el promedio de un número indeterminado de elementos, debemos utilizar argumentos variables. Para ello, simplemente agregamos un * delante del nombre del argumento, y luego podemos trabajar con él como si se tratara de una lista:

```py
def promedio(*num):
    return sum(num) / len(num)

print(promedio(1, 2, 3, 4)) # output: 2.5
print(promedio(1, 2)) # output: 1.5
print(promedio(3, 6, 9, 12, 15)) # output: 9
```

En este caso, la función `promedio` recibe un número indeterminado de elementos. A continuación, se calcula la suma de estos elementos con `sum(num)` y se divide entre la cantidad de elementos con `len(num)`.

Además de los argumentos variables con `*`, también podemos utilizar los argumentos variables con `**`. Estos son útiles para trabajar con diccionarios y para definir argumentos con nombre en una función. Por ejemplo, supongamos que tenemos un diccionario con el nombre y la edad de varias personas, y queremos crear una función que imprima el nombre y la edad de cada uno de ellos:

```py
def nombres_edades(**personas):
    for nombre, edad in personas.items():
        print(f'{nombre} tiene {edad} años.')

nombres_edades(Ana=20, Luis=30, Pedro=25)

# output:
# Ana tiene 20 años.
# Luis tiene 30 años.
# Pedro tiene 25 años.
```

En este caso, se utiliza `**personas` para indicar que la función recibirá un número indeterminado de argumentos con nombre, que se almacenarán en un diccionario. Dentro de la función, se utiliza un bucle para imprimir el nombre y la edad de cada persona.

>  
> 
> Los argumentos variables son una herramienta muy útil en Python, que nos permiten trabajar con un número indeterminado de elementos en una función. Los argumentos variables con `*` se utilizan para trabajar con listas y tuplas, mientras que los argumentos variables con `**` se utilizan para trabajar con diccionarios y para definir argumentos con nombre en una función. Con su uso, logramos dar mayor flexibilidad y adaptabilidad a nuestras funciones, lo cual es fundamental en programación.

## Cómo utilizar argumentos de longitud variable en Python

Las funciones son uno de los pilares fundamentales en la programación en Python. Una de las características más llamativas de las funciones en Python es la flexibilidad que brindan en cuanto al manejo de argumentos. En este artículo, nos enfocaremos en cómo utilizar argumentos de longitud variable en Python, lo que nos permite proporcionar una cantidad variable de argumentos a una función.

Para empezar, podemos definir una función que acepte cualquier cantidad de argumentos utilizando un único operador `*` antes del nombre del argumento. Por ejemplo, considera la siguiente función `imprimir_argumentos`:

```py
def imprimir_argumentos(*args):
    for arg in args:
        print(arg)
```

En este ejemplo, `args` será una tupla de todos los argumentos que se proporcionen a la función. Entonces, podemos llamar la función de esta manera:

```py
imprimir_argumentos(1, 2, 3)
```

Y la salida será:

```txt
1
2
3
```

Podemos proporcionar cualquier cantidad de argumentos, y la función los imprimirá todos. Este método es muy útil cuando queremos proporcionar muchos argumentos a una función sin tener que especificarlos todos en su firma.

Otra forma de manejar una cantidad variable de argumentos en Python es utilizando el doble operador `**`. Si usamos este operador antes del nombre de un argumento, Python creará un diccionario con los nombres de los argumentos como llaves y los valores como valores. Por ejemplo, considera la siguiente función `imprimir_kwargs`:

```py
def imprimir_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

Ahora, si llamamos esta función de la siguiente manera:

```py
imprimir_kwargs(nombre="Juan", edad=30)
```

La salida será:

```txt
nombre: Juan
edad: 30
```

Podemos proporcionar cualquier cantidad de argumentos con nombres diferentes, y la función los imprimirá todos.

Podemos combinar ambas técnicas para crear una función que maneje tanto argumentos sin nombre como argumentos con nombre. Por ejemplo:

```py
def imprimir_todo(*args, **kwargs):
    for arg in args:
        print(arg)

    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

Ahora, podemos llamar esta función de la siguiente manera:

```py
imprimir_todo(1, 2, 3, nombre="Juan", edad=30)
```

Y la salida será:

```txt
1
2
3
nombre: Juan
edad: 30
```

>  
> 
> Python ofrece una gran flexibilidad en cuanto al manejo de argumentos en funciones. Podemos utilizar argumentos de longitud variable para crear funciones con mayor adaptabilidad y flexibilidad. Esto nos permite crear funciones más versátiles y eficientes en nuestro código.

## Cómo manejar errores al pasar argumentos en Python

Cuando escribimos código en Python, es muy común que usemos funciones para modularizar nuestras tareas y tener un código más organizado y legible. Una de las ventajas de las funciones es que podemos enviarles argumentos, es decir, valores que la función puede usar para hacer su trabajo. En ocasiones, puede ocurrir que al pasar argumentos a una función, tengamos errores que hagan que nuestro programa falle.

Por ejemplo, imagine que tenemos una función llamada `sumar` que recibe dos números y devuelve la suma de estos. Si intentamos pasarle un argumento que no es un número, como una cadena de texto, obtendremos un error:

```py
def sumar(num1, num2):
    return num1 + num2

print(sumar(2, "3")) # genera TypeError
```

En este caso, obtendríamos un `TypeError` ya que Python no puede sumar un número con una cadena de texto. Para evitar errores como este, es importante manejar los argumentos que les pasamos a nuestras funciones.

Una forma de manejar estos errores es usando validaciones antes de ejecutar el código de nuestra función. Por ejemplo, podemos usar la función `isinstance` para comprobar que nuestros argumentos sean del tipo que esperamos:

```py
def sumar(num1, num2):
    if isinstance(num1, (int, float)) and isinstance(num2, (int, float)):
        return num1 + num2
    else:
        return "Error: los argumentos deben ser números"

print(sumar(2, "3")) # devuelve el mensaje de error
```

En este caso, estamos comprobando que `num1` y `num2` sean del tipo `int` o `float` antes de hacer la suma. Si no lo son, devolvemos un mensaje de error indicando que los argumentos deben ser números.

Otra opción es usar la función `try-except` para manejar los errores que puedan surgir al pasar argumentos a una función. Por ejemplo:

```py
def sumar(num1, num2):
    try:
        return num1 + num2
    except TypeError:
        return "Error: los argumentos deben ser números"

print(sumar(2, "3")) # devuelve el mensaje de error
```

En este caso, estamos intentando hacer la suma directamente dentro de la función. Si ocurre un error de tipo (`TypeError`), capturamos la excepción con el bloque `except` y devolvemos un mensaje de error indicando que los argumentos deben ser números.

>  
> 
> Manejar los errores al pasar argumentos a nuestras funciones en Python es una buena práctica para asegurarnos de que nuestro programa funcione correctamente. Podemos hacer esto usando validaciones o el manejo de excepciones, dependiendo del caso particular que queramos manejar. Con estas técnicas, aumentamos la flexibilidad y adaptabilidad de nuestras funciones, garantizando una mayor robustez y sencillez en la escritura del código.

## Consejos y buenas prácticas para el manejo de argumentos en funciones Python

Durante mi experiencia programando en Python, he aprendido que el manejo de argumentos en funciones es una de las cosas más importantes a tener en cuenta. La flexibilidad y adaptabilidad en el manejo de argumentos, pueden hacer que nuestras funciones sean más eficientes y mejor estructuradas.

Aquí te dejo algunos consejos y buenas prácticas que te pueden ayudar a manejar los argumentos en tus funciones de manera eficiente.

## Definir valores por defecto

Es buena práctica definir valores por defecto a los argumentos de nuestras funciones. Esto nos permite no tener problemas en caso de que alguno de los argumentos no sea pasado correctamente. Además, nos permite tener una manera fácil de sobrescribir estos valores en caso de que sea necesario.

Por ejemplo:

```py
def saludar(nombre, saludo='Hola'):
    print(saludo + ', ' + nombre)

saludar('Juan') # Output: Hola, Juan
saludar('Ana', 'Buenas tardes') # Output: Buenas tardes, Ana
```

En el ejemplo anterior, hemos definido un valor por defecto para el saludo. Si no pasamos ningún valor, el saludo será “Hola”. Si queremos sobrescribir este valor, simplemente pasamos un segundo argumento a la función.

## Utilizar argumentos posicionales y de palabras clave

Python permite el uso de argumentos posicionales y de palabras clave. Los argumentos posicionales son aquellos que son pasados en el orden en el que se definen en la función. Los argumentos de palabras clave son aquellos en los que se especifica el nombre del argumento antes de su valor.

Por ejemplo:

```py
def sumar(a, b):
    return a + b

sumar(3, 4) # Output: 7
sumar(a=3, b=4) # Output: 7
sumar(b=4, a=3) # Output: 7
```

En el ejemplo anterior, hemos definido una función que suma dos números. Podemos llamar la función tanto con argumentos posicionales, como con argumentos de palabras clave. Incluso podemos cambiar el orden de los argumentos de palabras clave sin afectar el resultado de la función.

## Manejar argumentos variables

En Python, podemos manejar argumentos variables utilizando el operador `*` en los argumentos de la función. De esta manera, podemos permitir que la función reciba un número variable de argumentos.

Por ejemplo:

```py
def promedio(*numeros):
    return sum(numeros) / len(numeros)

promedio(3, 4, 5) # Output: 4.0
promedio(1, 2, 3, 4, 5, 6, 7, 8, 9, 10) # Output: 5.5
```

En el ejemplo anterior, hemos definido una función que calcula el promedio de un número variable de argumentos. Utilizando el operador `*`, podemos pasar un número variable de argumentos a la función.

>  
> 
> El manejo de argumentos en funciones es una de las cosas más importantes a tener en cuenta al programar en Python. Definir valores por defecto, utilizar argumentos posicionales y de palabras clave, y manejar argumentos variables, son algunas de las buenas prácticas que te pueden ayudar a crear funciones más eficientes y mejor estructuradas. No dudes en seguir investigando y aprendiendo sobre este tema para mejorar tus habilidades como programador Python.