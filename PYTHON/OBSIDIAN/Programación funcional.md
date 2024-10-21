
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/programacion-funcional-en-python-enfoque-modular-y-reutilizable.webp)

## Introducción a la programación funcional en Python

¿Alguna vez te has preguntado cómo sería programar sin la necesidad de usar variables y sin tener que preocuparte por los efectos secundarios? La programación funcional es una forma de programar en la que se utilizan funciones puras para manipular datos, sin la necesidad de guardar estados en variables o cambiar el estado de un programa. En Python, podemos implementar una programación funcional de manera sencilla y modular.

La **programación funcional** se enfoca en la idea de que el código siempre debe de producir el mismo resultado, dadas las mismas entradas. Esto significa que las funciones en programación funcional nunca deberían tener efectos secundarios. Un efecto secundario es cualquier acción que la función realiza que no tiene nada que ver con su salida. Por ejemplo, una función que escribe a un archivo en disco tiene un efecto secundario.

La programación funcional ofrece muchas ventajas. En primer lugar, los **programas son más fáciles de leer y comprender**, ya que las funciones suelen ser más simples y fáciles de entender. En segundo lugar, los programas son más modulares y fáciles de mantener. Cada función es independiente de las demás, lo que permite cambiar su comportamiento sin afectar el resto del programa.

En Python, podemos **implementar una programación funcional utilizando las funciones lambda y las funciones puras**. Las funciones lambda son funciones anónimas que pueden ser utilizadas como argumentos de otras funciones. Por ejemplo, podemos usar una función lambda para crear una lista con los números del 1 al 10 elevados al cuadrado:

```py
>>> lista = list(map(lambda x: x**2, range(1,11)))
>>> print(lista)
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

**Las funciones puras**, por otro lado, son aquellas que nunca modifican el estado de un programa y siempre producen el mismo resultado para las mismas entradas. Esto hace que las funciones puras sean más fáciles de entender y depurar. Por ejemplo, la función siguiente es una función pura que dado un número, devuelve su valor absoluto:

```py
def valor_absoluto(n):
    if n < 0:
        return -n
    else:
        return n
```

>  
> 
> La programación funcional en Python ofrece una forma modular y reutilizable de programar, usando funciones puras y funciones lambda. Las funciones puras permiten escribir programas más fáciles de entender y depurar, mientras que las funciones lambda permiten escribir programas más concisos y legibles. En los siguientes capítulos, exploraremos más a fondo la programación funcional en Python, aprendiendo a crear y utilizar funciones puras y funciones lambda en nuestros programas.

## Ventajas de la programación funcional frente a la programación imperativa

**La programación funcional** es una técnica de programación que en los últimos años ha ganado mucha popularidad. Cuando hablamos de programación funcional nos referimos a un enfoque de programación que se enfoca en construir programas a partir de funciones. A diferencia de la programación imperativa en la que se definen estados y se modifican durante el programa, en la programación funcional no se utilizan estados sino funciones para resolver problemas.

Existen varias **ventajas de la programación funcional sobre la programación imperativa**. Una de las más importantes es que es más fácil de entender y de mantener el código. Cuando un programa está construido a partir de funciones, todas las funciones se pueden utilizar en diferentes partes del programa sin tener que preocuparse por los efectos secundarios que podrían provocar los cambios de estado. Esto significa que es más fácil entender la lógica del programa y más sencillo corregir errores una vez que se han detectado.

Otra ventaja de **la programación funcional es que es más fácil de debuggear**. Cuando un programa está construido a partir de funciones, es más fácil desglosar el programa en pequeñas partes y probar cada función por separado. Esto significa que los errores se pueden detectar y arreglar más fácilmente. Además, las funciones son más fáciles de testear unitariamente porque no tienen dependencias externas.

**La programación funcional también es más reutilizable**. Cuando uno construye un programa a partir de funciones reutilizables, se pueden utilizar estas funciones en diferentes partes del código sin tener que preocuparse por los efectos secundarios de los cambios de estado. Además, una vez que se han creado estas funciones reutilizables, se pueden utilizar en diferentes programas y proyectos sin tener que volver a escribirlas.

Un ejemplo de cómo se puede aplicar la programación funcional en Python es a través del uso del modulo `map`. `map` es una función que se utiliza para aplicar una función a cada elemento de un iterable. Por ejemplo, si queremos aplicar la función `square` a cada elemento de una lista podemos utilizar la función `map` de la siguiente forma:

```py
def square(x):
  return x*x

numbers = [1, 2, 3, 4, 5]

squared_numbers = list(map(square, numbers))
```

En este ejemplo, primero definimos la función `square`. Luego creamos una lista `numbers` que contiene los números a los cuales aplicaremos la función `square`. Finalmente utilizamos la función `map` para aplicar `square` a cada elemento de la lista `numbers`. El resultado es una lista `squared_numbers` que contiene los cuadrados de cada uno de los elementos de `numbers`.

>  
> 
> La programación funcional es un enfoque de programación con muchas ventajas. A través del uso de funciones reutilizables, podemos construir programas más sencillos de entender, mantener y debuggear. Además, una vez que se han definido estas funciones reutilizables, las podemos utilizar en diferentes programas y proyectos sin tener que volver a escribirlas.

## Cómo utilizar funciones lambda y de orden superior en Python

Al **trabajar con programación funcional en Python**, uno de los conceptos más importantes es el de funciones lambda y de orden superior. Estas herramientas pueden ayudar a hacer que nuestro código sea más modular y reutilizable, permitiéndonos crear funciones más complejas y expresivas.

**Una función lambda es una función anónima que se puede definir en una sola linea de código**. En lugar de usar la palabra clave `def` con un nombre de función, podemos definir una función lambda utilizando la palabra clave `lambda`. Por ejemplo, supongamos que queremos encontrar el cuadrado de un numero. Podríamos escribir una función lambda de la siguiente manera:

```py
square = lambda x: x**2
```

Como puedes ver, la función lambda utiliza la sintaxis `lambda x:` para indicar que esta recibiendo un parámetro `x`, seguido de la expresión `x**2` para indicar la operación que queremos realizar. Podemos llamar a esta función lambda de la misma forma que llamaríamos a cualquier otra función, por ejemplo:

```py
>>> square(5)
25
```

También podemos utilizar funciones lambda en conjunto con otras funciones, como `map()` y `filter()`. Por ejemplo, supongamos que tenemos una lista de numeros y queremos crear una nueva lista que contenga el cuadrado de cada numero. Podríamos utilizar la función `map()` junto con una función lambda para lograr esto. La sintaxis sería la siguiente:

```py
numbers = [1, 2, 3, 4, 5]
squares = map(lambda x: x**2, numbers)
```

En este ejemplo, la función lambda `lambda x: x**2` se aplica a cada elemento de la lista `numbers` utilizando la función `map()`, y se crea una nueva lista llamada `squares` que contiene el cuadrado de cada numero en la lista original.

Además de las funciones lambda, también podemos **utilizar funciones de orden superior en Python**. Estas son funciones que toman otras funciones como argumentos o devuelven funciones como resultado. Un ejemplo común de una función de orden superior es `sorted()`, que toma una lista como argumento y devuelve una lista ordenada utilizando un criterio de ordenamiento específico. Podemos utilizar la función `sorted()` junto con una función lambda como criterio de ordenamiento. Por ejemplo:

```py
words = ['apple', 'banana', 'cherry', 'durian', 'elderberry']
sorted_words = sorted(words, key=lambda x: x[-1])
```

En este ejemplo, la función lambda `lambda x: x[-1]` se utiliza como criterio de ordenamiento al pasarla como argumento a la función `sorted()`. La función lambda toma cada elemento de la lista `words` y devuelve el ultimo caracter de cada elemento (es decir, la letra “e” en el caso de “apple”, “a” en el caso de “banana”, etc.). La lista `sorted_words` contiene los elementos de la lista `words` ordenados alfabéticamente según la última letra de cada palabra.

>  
> 
> Las funciones lambda y de orden superior son herramientas extremadamente útiles cuando se trabaja con programación funcional en Python. Nos permiten crear funciones más expresivas y modulares, y también nos permiten utilizar funciones como argumentos o resultado en otras funciones. Si todavía no estas utilizando funciones lambda y de orden superior en tus proyectos de Python, te sugerimos que comiences a considerar su uso.

## Ejemplos de programación funcional en cadenas de texto y listas

En programación funcional, se enfatiza la **composición y aplicación de funciones en lugar de la manipulación directa de variables y objetos**. Esto permite un enfoque modular y reutilizable para el desarrollo de software, lo que a su vez puede simplificar el mantenimiento y la escalabilidad. En Python, hay varias herramientas integradas para programación funcional que pueden simplificar la escritura de código y mejorar su rendimiento.

En cadenas de texto, la programación funcional se puede utilizar para transformar y filtrar datos de manera eficiente. Por ejemplo, para contar el número de palabras en una cadena, se puede utilizar la función `split` para separar la cadena en una lista de palabras y luego aplicar la función `len` para obtener la longitud de la lista resultante:

```py
texto = "Esto es una cadena de ejemplo"
palabras = texto.split()
numero_palabras = len(palabras)
```

Del mismo modo, para filtrar las palabras que comienzan con una letra específica, se puede utilizar la función `filter` junto con una función lambda para aplicar el filtro:

```py
texto = "Esto es una cadena de ejemplo"
palabras = texto.split()
palabras_filtradas = list(filter(lambda palabra: palabra.startswith("e"), palabras))
```

La lista resultante `palabras_filtradas` contiene solo las palabras que comienzan con “e”.

En las listas, la programación funcional también puede ser útil para realizar operaciones en lotes, como la suma o el producto de todos los elementos. Para hacer esto, se pueden utilizar las funciones `reduce` y `operator`, que permiten aplicar una operación a todos los elementos de una lista de manera cuantitativa y eficiente:

```py
from functools import reduce
import operator

lista_numeros = [1, 2, 3, 4, 5]
suma_numeros = reduce(operator.add, lista_numeros)
producto_numeros = reduce(operator.mul, lista_numeros)
```

La variable `suma_numeros` contendrá la suma de todos los elementos de la lista, mientras que la variable `producto_numeros` contendrá el producto de todos los elementos de la lista.

>  
> 
> La programación funcional en Python puede ser muy poderosa para manipular cadenas de texto y listas de manera modular y reutilizable. Al usar técnicas como la composición y la aplicación de funciones en lotes, el código puede ser más fácil de leer y mantener, lo que puede simplificar significativamente el desarrollo de software.

## Crear módulos para reutilizar código funcional en distintos proyectos

Creando módulos para reutilizar código funcional en distintos proyectos

Cuando se trabaja en varios proyectos de programación, es común encontrar patrones de código que se repiten constantemente. Esto puede llevar a una redundancia innecesaria y a un código más difícil de actualizar. Para abordar este problema, muchos programadores utilizan módulos reutilizables que contienen funciones específicas que se pueden importar en diferentes proyectos.

**La programación funcional es ideal para crear módulos reutilizables debido a su enfoque modular**. Cada función es independiente y se centra en hacer una tarea específica, lo que las hace fácilmente transportables de un proyecto a otro.

En Python, puede crear un módulo simplemente creando un archivo con una extensión `.py`. Dentro de este archivo, puede crear todas las funciones que desee, al igual que en cualquier otro archivo de Python. La única diferencia es que cualquiera que importe este archivo tendrá acceso a estas funciones.

Vamos a crear un ejemplo simple de un módulo que contiene dos funciones. La primera función calcula la suma de dos números, y la segunda función calcula la diferencia entre dos números. El código sería así:

```py
def suma(a, b):
    return a + b

def diferencia(a, b):
    return a - b
```

Para utilizar estas funciones en otro archivo de Python, debemos primero importar el módulo. Lo podemos hacer con la sentencia `import`, seguido del nombre del archivo sin la extensión `.py`. Aquí está el código que utilizaría estas funciones en otro archivo:

```py
import mi_modulo

resultado = mi_modulo.suma(2, 4)
print(resultado) # resultado es 6

resultado2 = mi_modulo.diferencia(8, 3)
print(resultado2) # resultado2 es 5
```

De esta manera, podemos reutilizar nuestras funciones de manera fácil y efectiva en cualquier proyecto que estemos trabajando. Por supuesto, esto es solo un ejemplo simple; los módulos pueden contener cualquier cantidad de funciones, dependiendo de las necesidades del proyecto.

Es importante tener en cuenta que al crear módulos, estamos creando componentes reutilizables que pueden ahorrar una gran cantidad de tiempo y esfuerzo en proyectos futuros. Saber cómo crear y utilizar módulos es una habilidad valiosa para cualquier programador, y la programación funcional es una forma efectiva de hacerlo.

>  
> 
> Crear módulos reutilizables en Python es una forma efectiva de maximizar la eficiencia en proyectos futuros. La programación funcional es un enfoque excelente para crear módulos, ya que se centran en la creación de funciones independientes y específicas. Con la capacidad de reutilizar funciones a través de múltiples proyectos, los módulos son una herramienta invaluable para cualquier programador.

## Manejo de errores en programación funcional

La programación funcional en Python ofrece muchas ventajas, como la **modularidad y la reutilización de código**. Sin embargo, uno de los mayores desafíos que se presentan al trabajar con esta metodología es el manejo de errores.

En lugar de **manejar los errores en un bloque try-catch** como se hace en la programación imperativa, la programación funcional utiliza una técnica llamada “monads”. Los monads son una abstracción matemática que permite manejar efectos secundarios, como los errores y los cambios en el estado, en la programación funcional.

**Los monads son estructuras de datos que encapsulan un valor y una función que transforma ese valor en otro valor encapsulado**. En el caso del manejo de errores, se utiliza un tipo de monad llamado “maybe”, que puede representar un valor que puede faltar o un error.

Para **manejar errores con monads en Python**, se puede utilizar la biblioteca “pymonad”. Por ejemplo, supongamos que queremos dividir dos números y manejar el posible error de división por cero.

```py
from pymonad.Maybe import Just, Nothing

def divide(a, b):
    if b == 0:
        return Nothing
    else:
        return Just(a / b)
```

En esta función, si b es igual a cero, se devuelve un monad de tipo “Nothing”, que representa un valor que falta. De lo contrario, se devuelve un monad “Just” que contiene el resultado de la división.

Para acceder al valor encapsulado dentro de un monad, se utiliza el método “getValue”. Si se trata de un valor “Just”, se devuelve el valor. Si es un valor “Nothing”, se produce una excepción.

```py
result = divide(4, 2).getValue() # devuelve 2.0
result = divide(4, 0).getValue() # produce una excepción
```

Además del monad “maybe”, también se pueden utilizar otros tipos de monads para manejar diferentes efectos secundarios, como los cambios en el estado.

>  
> 
> El manejo de errores en la programación funcional requiere el uso de monads, que son estructuras de datos que encapsulan un valor y una función que transforma ese valor en otro valor encapsulado. En Python, se puede utilizar la biblioteca “pymonad” para manejar errores con monads.

## Utilización de decoradores para añadir funcionalidades a nuestras funciones

Los **decoradores** son una forma de añadir **funcionalidades** adicionales a nuestras **funciones**, sin modificar su código original. Permiten cambiar el comportamiento de una función sin tener que reescribirla por completo. En Python, los decoradores se definen utilizando la notación de **@decorador** antes de la definición de la función que se desea decorar.

La sintaxis básica de un decorador es la siguiente:

```py
def decorador(funcion_original):
    def funcion_decorada():
        # Código que se ejecuta antes de la función original
        resultado = funcion_original()
        # Código que se ejecuta después de la función original
        return resultado
    return funcion_decorada

@decorador
def funcion_original():
    # Código de la función original
    return resultado
```

En este ejemplo, el decorador toma la función original como argumento y utiliza una nueva función para añadirle funcionalidad. La función decorada es la que se llama en su lugar, y ésta a su vez invoca a la función original. De esta forma, podemos insertar código que se ejecute antes o después de la función original, o incluso modificar el valor devuelto por la función.

Un ejemplo de decorador podría ser el siguiente:

```py
def log(funcion_original):
    def funcion_decorada(*args, **kwargs):
        print(f"Llamando a la función {funcion_original.__name__}")
        resultado = funcion_original(*args, **kwargs)
        print(f"La función {funcion_original.__name__} devolvió {resultado}")
        return resultado
    return funcion_decorada

@log
def suma(a, b):
    return a + b

resultado = suma(2, 3)
```

En este caso, el decorador **log** añade funcionalidad de registro de log, imprimiendo un mensaje antes y después de llamar a la función original. La notación `*args, **kwargs` indica que la función puede recibir un número variable de argumentos y palabras clave.

Los decoradores son especialmente útiles en la programación funcional, ya que permiten separar la lógica de control de la lógica de negocio. Además, son una forma elegante de extender el comportamiento de nuestras funciones sin tener que repetir código.

### Algunos ejemplos de decoradores comunes en Python son:

- `@classmethod`: indica que la función es un método de clase en lugar de un método de instancia.
- `@staticmethod`: indica que la función no utiliza información de la clase ni de la instancia.
- `@property`: convierte un método en una propiedad, que puede ser accedida como un atributo de la instancia.

En resumen, los decoradores son una herramienta poderosa y versátil en Python, que permiten añadir funcionalidad a nuestras funciones de forma elegante y modular. Al utilizarlos, podemos separar la lógica de control de la lógica de negocio, y extender el comportamiento de nuestras funciones de forma sencilla y reutilizable.

## El poder de la inmutabilidad en programación funcional

La **programación funcional** se basa en funciones que no mutan los valores de entrada y no tienen efectos secundarios imprevistos. Es decir, se enfoca en trabajar con datos inmutables en lugar de datos mutables, lo que permite crear programas más simples, robustos y reutilizables.

La **inmutabilidad** es un concepto clave en programación funcional, ya que los datos inmutables no pueden ser modificados una vez que se han creado. Esto significa que, en lugar de modificar los datos existentes, se crean nuevos con los cambios necesarios. De esta manera, los valores se mantienen consistentes y es más fácil mantener el control sobre ellos.

En Python, los objetos mutables son aquellos que pueden cambiar sus valores internos después de que se han creado, mientras que los objetos inmutables no pueden ser modificados. Algunos ejemplos de objetos inmutables en Python son las cadenas, los números y las tuplas.

Veamos un ejemplo para entender mejor el poder de la inmutabilidad en programación funcional. Imagina que queremos sumar los elementos de una lista de números. Una solución intuitiva sería crear una variable `total` y agregar los elementos uno por uno en un bucle:

```py
def sumar_numeros(lista):
    total = 0
    for num in lista:
        total += num
    return total

numeros = [1, 2, 3, 4, 5]
print(sumar_numeros(numeros)) # Output: 15
```

Sin embargo, esta solución no es inmutable, ya que estamos modificando la variable `total` en cada iteración del bucle. En programación funcional, preferimos soluciones más inmutables, como la siguiente:

```py
def sumar_numeros_inmutable(lista):
    if lista == []:
        return 0
    else:
        return lista[0] + sumar_numeros_inmutable(lista[1:])

numeros = [1, 2, 3, 4, 5]
print(sumar_numeros_inmutable(numeros)) # Output: 15
```

Este código utiliza una **función recursiva** para sumar los valores de la lista de manera inmutable. En lugar de modificar una variable en cada iteración, la función crea una nueva lista cada vez que se llama recursivamente, pasando como argumento la lista original sin el primer elemento. El código finalmente devuelve la suma de los elementos de la lista.

**La inmutabilidad** es una herramienta poderosa para crear programas más robustos y reutilizables en programación funcional. Al trabajar con datos inmutables, podemos eliminar muchos de los efectos secundarios imprevistos que pueden causar errores en nuestro programa. Además, la inmutabilidad nos permite crear funciones más simples y modulares, que podemos reutilizar en diferentes contextos sin tener que preocuparnos por el estado del programa.

>  
> 
> En resumen, la inmutabilidad es un concepto fundamental en programación funcional. Al trabajar con datos inmutables, podemos crear soluciones más robustas y reutilizables, lo que nos permite construir programas más eficientes y fáciles de mantener.

## Programación funcional para procesamiento de datos en ciencia de datos

La programación funcional se ha convertido en una herramienta fundamental para procesar grandes cantidades de datos en el campo de la ciencia de datos. Con el uso de la programación funcional en Python, podemos llevar el procesamiento de datos a un nuevo nivel de modularidad y reutilización.

En nuestra experiencia, hemos notado una gran diferencia en la **eficiencia del procesamiento de datos al utilizar programación funcional**. En lugar de trabajar con grandes bloques de código, podemos estructurar nuestro código en pequeños componentes modulares que se pueden reutilizar y ajustar en diferentes proyectos.

Una de las **claves para programar de manera funcional** es trabajar con funciones puras que no tienen efectos secundarios. Esto significa que no modifican variables fuera de su alcance y siempre devuelven un resultado predecible. Al trabajar con funciones puras, podemos evitar errores comunes que pueden surgir al trabajar con datos en ciencia de datos.

Siguiendo los **principios de programación funcional**, también podemos utilizar de manera más eficiente los recursos del equipo. En lugar de procesar grandes conjuntos de datos de una sola vez, podemos dividir el proceso en pequeñas tareas más manejables y ejecutarlas en paralelo para aprovechar al máximo la capacidad de procesamiento. Podemos utilizar la biblioteca de multiprocesamiento de Python para llevar a cabo esta tarea de manera eficiente.

Tomemos como ejemplo el procesamiento de un gran conjunto de datos que contiene información sobre consumidores y ventas. Podemos estructurar este proceso como una serie de tareas más pequeñas, como la agrupación de datos, la agregación de estadísticas y la visualización de resultados. Cada una de estas tareas puede implementarse como una función pura independiente.

Definir funciones puras para cada tarea nos permite reutilizar estas funciones en diferentes proyectos sin tener que volver a escribir todo el código. También nos permite hacer ajustes específicos a cada tarea según las necesidades de cada proyecto.

Veamos un ejemplo práctico de una función que procesa una columna determinada de un dataframe en pandas. Esta función toma como entrada el dataframe y el nombre de la columna a procesar y devuelve un nuevo dataframe con la columna procesada.

```py
import pandas as pd
def process_column(df, column_name):
    new_df = df.copy()
    new_df[column_name] = new_df[column_name].apply(lambda x: x * 2)
    return new_df
```

>  
> 
> La programación funcional ofrece un enfoque modular y reutilizable para procesar grandes cantidades de datos que es especialmente útil en el campo de la ciencia de datos. Al utilizar funciones puras y estructurar nuestro código en tareas más pequeñas, podemos aumentar la eficiencia y la capacidad de procesamiento de nuestro equipo. ¡Anímate a probar la programación funcional en tus próximos proyectos de ciencia de datos!

## Principales librerías y frameworks de programación funcional en Python

Una de las **ventajas de la programación funcional** es que cuenta con diversas librerías y frameworks que facilitan el desarrollo de aplicaciones y la implementación de patrones de diseño. En Python, existen varias opciones que se pueden aplicar a proyectos de cualquier tamaño y complejidad. A continuación, presentamos algunas de las principales librerías y frameworks de programación funcional en Python.

## NumPy

NumPy es una librería que se enfoca en la manipulación y operaciones con arreglos y matrices. Es muy popular en la comunidad científica debido a que es muy eficiente en la ejecución de cálculos numéricos y estadísticos. Esta librería es una herramienta indispensable para el análisis de datos y la implementación de modelos de machine learning.

```py
import numpy as np

# Crear un arreglo de 5 elementos
arr = np.array([1, 2, 3, 4, 5])
print(arr)

# Operaciones matemáticas con arreglos
arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])
print(arr1 + arr2)
```

## Pandas

Pandas es otra librería importante para el manejo de datos. Se enfoca en la estructuración y manipulación de datos en forma de tablas y dataframes. Con Pandas, se pueden realizar operaciones de filtrado, agrupación y transformación de datos de manera muy eficiente.

```py
import pandas as pd

# Crear un dataframe
data = {'nombre': ['Juan', 'Pedro', 'María'], 'edad': [25, 30, 28]}
df = pd.DataFrame(data)
print(df)

# Filtrar por edad mayor a 26
mayores = df[df['edad'] > 26]
print(mayores)
```

## Flask

Flask es un micro-framework para crear aplicaciones web en Python. Se caracteriza por su simplicidad y facilidad de aprendizaje. Aunque no es exclusivamente una herramienta de programación funcional, se presta muy bien para implementar patrones y técnicas de este paradigma. Flask es especialmente útil para proyectos pequeños o medianos que requieren una implementación rápida.

```py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return 'Hola mundo'

if __name__ == '__main__':
    app.run()
```

## Django

Django es un framework de desarrollo web full-stack que se enfoca en la eficiencia y la reutilización de código. Aunque no es una herramienta puramente de programación funcional, es compatible con este paradigma y se puede implementar fácilmente en proyectos de gran envergadura.

```py
from django.urls import path
from .views import home

urlpatterns = [
    path('', home, name='home'),
]
```

## functools

La librería functools es una herramienta muy útil que contiene funciones de orden superior (higher-order functions) que permiten la composición de funciones y la creación de funciones parciales. Es especialmente útil en la implementación de patrones de diseño y soluciones de programación funcional.

```py
import functools

# Crear una función parcial
def suma(a, b):
    return a + b

suma5 = functools.partial(suma, 5)
print(suma5(3))
```

Estas son solo algunas de las librerías y frameworks disponibles en Python para implementar programación funcional. Cada una se presta para diferentes tipos de proyectos, y puedes mezclarlas y combinarlas según tus necesidades. La programación funcional en Python te permite escribir código modular y reusable, y te ayuda a mejor la legibilidad de tu código.