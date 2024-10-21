
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/decoradores-en-python-mejora-y-personalizacion-de-funciones.webp)

## Introducción a los decoradores en Python

Los **decoradores en Python** son una funcionalidad muy poderosa que permite mejorar la funcionalidad de las funciones de una manera muy sencilla. En resumen, un decorador se encarga de modificar el comportamiento de una función sin alterar su código.

Este concepto puede parecer un tanto abstracto al principio, por eso quiero compartir con ustedes nuestra experiencia utilizando decoradores en nuestro proyecto. Como equipo de desarrolladores, a menudo trabajamos con funciones que reciben muchos argumentos y, en ocasiones, se vuelven bastante difíciles de manejar. Fue en este momento que descubrimos los decoradores en Python y rápidamente nos dimos cuenta de su gran utilidad.

Para aquellos que no conocen los decoradores, imagina que tienes una función que recibe tres argumentos, pero te das cuenta de que debes añadir nuevos argumentos para hacerla más útil. Si simplemente añades estos nuevos argumentos, tendrás que modificar todas las instrucciones en el código que hacen referencia a esa función, lo que puede llevar mucho tiempo y generar errores.

En cambio, utilizando un decorador, puedes agregar los nuevos argumentos sin modificar el cuerpo de la función. En esencia, el decorador es una función que envuelve la función original y la modifica para que haga lo que necesitas con los nuevos argumentos.

Por ejemplo, supongamos que tienes una función llamada “funcion_principal” que acepta tres argumentos: “a”, “b”, y “c”. Quieres agregar dos nuevos argumentos, “d” y “e”, sin modificar la función original. Aquí es donde entra en juego el decorador. Podemos escribir una nueva función llamada “decorador_funcion_principal”, que toma “funcion_principal” como argumento y modifica su comportamiento.

```py
def decorador_funcion_principal(funcion_original):
    def nueva_funcion(a, b, c, d, e):
        resultado = funcion_original(a, b, c)
        # Hacer algo con los nuevos argumentos...
        return resultado

    return nueva_funcion
```

En nuestro ejemplo, la función “funcion_principal” no tiene que saber nada sobre los nuevos argumentos “d” y “e”. Todo lo que necesita hacer es devolver el resultado de los primeros tres argumentos, y el decorador se encargará del resto.

```py
@decorador_funcion_principal
def funcion_principal(a, b, c):
    return a + b + c
```

Una vez que hemos definido el decorador, podemos utilizarlo en nuestra función original utilizando el símbolo “@”.

Ahora la función “funcion_principal” se ha mejorado sin necesidad de modificar su código original. El decorador ha añadido la funcionalidad extra sin alterar la lógica de la función.

>  
> 
> Los decoradores en Python son una forma poderosa de mejorar y personalizar tus funciones sin modificar su código original. Si trabajas con funciones que reciben muchos argumentos, los decoradores son una herramienta útil que pueden ayudar a simplificar tu código y mejorar su eficiencia.

## Simplificación de la estructura de una función

Cuando empecé a programar en Python, me encontré escribiendo funciones voluminosas, llenas de if-else anidados y argumentos complicados. En un momento dado, sentía que estaba trabajando en código confuso e inmanejable. Fue entonces cuando descubrí los **decoradores en Python** y cómo pueden simplificar drásticamente la estructura de una función.

**Un decorador es una función especial que toma otra función y la transforma en una nueva función con nuevas características**. Por ejemplo, puede agregar una verificación de autorización o medición de tiempo a una función ya existente sin tener que reescribir la función en sí. Esto hace que el código sea más limpio y legible.

La sintaxis de un decorador es bastante simple. Primero, define la función decoradora, que toma la función que se va a decorar como argumento. Dentro de la función decoradora, se define una nueva función que agrega las características deseadas. Por último, la función decoradora devuelve la nueva función.

Por ejemplo, digamos que tenemos una función que realiza una tarea costosa y queremos medir el tiempo que tarda en ejecutarse. Podríamos hacerlo en bruto de la siguiente manera:

```py
import time

def mi_funcion(parametro):
    inicio = time.time()

    # El cuerpo de la función aquí...

    fin = time.time()
    tiempo_transcurrido = fin - inicio
    print("Función tardó {} segundos en ejecutarse".format(tiempo_transcurrido))
```

Sin embargo, esto es desordenado y dificulta la lectura de la función en sí. En su lugar, podemos utilizar un decorador que maneje la medición del tiempo por nosotros:

```py
import time

def medir_tiempo(funcion):
    def funcion_decorada(*args, **kwargs):
        inicio = time.time()

        resultado = funcion(*args, **kwargs)

        fin = time.time()
        tiempo_transcurrido = fin - inicio
        print("Función tardó {} segundos en ejecutarse".format(tiempo_transcurrido))

        return resultado

    return funcion_decorada
```

Ahora, para usar este decorador, simplemente lo aplicamos a nuestra función original con el símbolo @:

```py
@medir_tiempo
def mi_funcion(parametro):
    # El cuerpo de la función aquí...
```

Y eso es todo. Ahora nuestra función se ejecutará y mostrará la cantidad de tiempo que tardó en completarse sin tener que agregar código adicional a la propia función.

>  
> 
> Los decoradores son una herramienta poderosa en Python que pueden ayudar a simplificar la estructura de las funciones. Con solo unas pocas líneas de código, se pueden agregar características como medición de tiempo, autorización y mucho más. Si te encuentras escribiendo funciones complicadas y difíciles de leer, ¡prueba los decoradores en tu próximo proyecto y observa la diferencia que pueden hacer!

## Aumento de la eficiencia de las funciones

En nuestro equipo, nos hemos encontrado en varias ocasiones con el problema de que nuestras funciones en Python no eran lo suficientemente eficientes. Ya sea que estuviéramos trabajando con grandes conjuntos de datos o realizando operaciones complejas, nuestras funciones a menudo tardaban demasiado tiempo en completarse.

Sin embargo, gracias a los **decoradores** en Python, hemos descubierto una manera de mejorar significativamente la eficiencia de nuestras funciones. Los decoradores son una herramienta poderosa que permite agregar funcionalidades adicionales a una función existente sin tener que modificar su código. Esto nos ha permitido mejorar nuestras funciones sin tener que reescribir todo el código desde cero.

Por ejemplo, en una de nuestras aplicaciones estábamos trabajando con grandes cantidades de datos y nuestras funciones se estaban ejecutando muy lentamente. Sin embargo, gracias a un decorador que implementamos, pudimos mejorar la eficiencia de manera significativa. El decorador que usamos básicamente permitió que una función se ejecute solo si los argumentos de entrada son diferentes de los argumentos anteriores. De esta manera, solo se volvería a ejecutar la función si es necesario, lo que significó un gran ahorro de tiempo.

```py
def memoize(func):
    cache = {}
    def wraps(*args):
        if args in cache:
            return cache[args]
        else:
            res = func(*args)
            cache[args] = res
            return res

    return wraps
```

Este es solo un ejemplo de cómo los decoradores nos han permitido mejorar la eficiencia de nuestras funciones. En otro caso, estábamos trabajando en una aplicación que requería cálculos complejos y que también teníamos que realizar con frecuencia. En lugar de tener que escribir el mismo código repetidamente, pudimos utilizar un decorador para guardar el resultado en caché. Esto nos permitió ahorrar tiempo y evitar recalculaciones innecesarias.

```py
def cache(func):
    saved = {}
    def wraps(*args):
        if args in saved:
            return saved[args]
        else:
            res = func(*args)
            saved[args] = res
            return res

    return wraps
```

En general, hemos encontrado que al utilizar decoradores en nuestras aplicaciones de Python, podemos **mejorar significativamente la eficiencia de nuestras funciones**, lo que nos permite **procesar grandes cantidades de datos de manera más efectiva y ahorrar tiempo en el desarrollo de la aplicación**. Los decoradores que hemos implementado son solo algunos ejemplos y existen muchas más formas de utilizarlos en la implementación de software. A medida que continuamos evolucionando nuestras habilidades de programación, esperamos descubrir aún más maneras de utilizar esta herramienta poderosa para mejorar el desempeño de nuestras aplicaciones.

## Personalización de las funciones para adaptarse a las necesidades específicas

Cuando programamos en Python, a menudo nos encontramos con la necesidad de **adaptar nuestras funciones a situaciones y casos particulares**. Sin embargo, modificar nuestras funciones para satisfacer estas necesidades específicas puede ser un proceso tedioso y repetitivo. Es aquí donde los decoradores en Python nos ofrecen una solución elegante y eficiente.

Los decoradores en Python son funciones que modifican el comportamiento de otras funciones sin cambiar su código subyacente. Es decir, nos permiten agregar funcionalidades adicionales a nuestras funciones sin tener que reescribir todo el código.

Para personalizar nuestras funciones, podemos utilizar los decoradores incorporados en Python, como “@staticmethod” y “@classmethod”, o crear nuestros propios decoradores personalizados.

Supongamos que tenemos una función llamada “saludar” que imprime un saludo en pantalla. Si queremos agregar un mensaje personalizado para cada usuario, podemos utilizar un decorador personalizado de la siguiente manera:

```py
def personalizar_saludo(func):
    def wrapper(nombre):
        mensaje = "¡Hola, {}! ¡Bienvenido de nuevo!".format(nombre)
        func(mensaje)
    return wrapper

@personalizar_saludo
def saludar(mensaje):
    print(mensaje)
```

En este caso, hemos creado un decorador personalizado llamado `personalizar_saludo` que toma una función y retorna una nueva función `wrapper` que agrega un mensaje personalizado a la función original y la ejecuta.

Luego, hemos decorado nuestra función `saludar` con el decorador personalizado `@personalizar_saludo`. Ahora, cada vez que llamemos a la función `saludar`, se ejecutará primero el decorador personalizado y se imprimirá un mensaje personalizado para el usuario.

Otro ejemplo podría ser si queremos medir el tiempo de ejecución de una función. Podemos utilizar un decorador personalizado para esto de la siguiente manera:

```py
import time

def medir_tiempo(func):
    def wrapper(*args, **kwargs):
        t_inicio = time.time()
        resultado = func(*args, **kwargs)
        t_final = time.time()
        print("La función {} se ejecutó en {} segundos.".format(func.__name__, t_final - t_inicio))
        return resultado
    return wrapper

@medir_tiempo
def suma_numeros(lista_numeros):
    resultado = sum(lista_numeros)
    return resultado
```

En este ejemplo, hemos creado un decorador personalizado llamado “medir_tiempo” que toma una función y retorna una nueva función “wrapper” que mide el tiempo de ejecución de la función original y la ejecuta.

Luego, hemos decorado nuestra función “suma_numeros” con el decorador personalizado “@medir_tiempo”. Ahora, cada vez que llamemos a la función “suma_numeros”, se ejecutará primero el decorador personalizado y se medirá el tiempo de ejecución de la función.

>  
> 
> Los decoradores en Python son una herramienta poderosa que nos permiten personalizar nuestras funciones para adaptarlas a necesidades específicas sin tener que reescribir todo el código. Podemos utilizar los decoradores incorporados en Python o crear nuestros propios decoradores personalizados para agregar funcionalidades adicionales a nuestras funciones de manera eficiente y elegante.

## Mejoramiento de la legibilidad y mantenibilidad del código

Al utilizar **decoradores** en Python, se pueden mejorar significativamente la legibilidad y mantenibilidad del código. Un buen decorador puede hacer que el código sea más fácil de leer, más intuitivo y más escalable.

Uno de los problemas comunes en el desarrollo de software es la repetitividad. Cuando se tiene que implementar la misma funcionalidad en muchas funciones, puede resultar en un código difícil de leer y es propenso a errores. Esto puede ser solucionado mediante el uso de decoradores.

Un ejemplo sencillo es la función que imprime el resultado de una operación:

```py
def add_numbers(a, b):
    return a + b

def print_result(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        print(f"Resultado: {result}")
        return result
    return wrapper

add_numbers = print_result(add_numbers)

add_numbers(4, 5) # Resultado: 9
```

En este caso, la función `print_result` actúa como un decorador que se encarga de imprimir el resultado de otra función (`add_numbers`). La idea central es que, al haber separado la funcionalidad de imprimir el resultado, podemos reutilizar esta en otras funciones similares sin tener que repetir el mismo código.

Además, este enfoque hace que el código sea mucho más fácil de leer. En lugar de tener la impresión del resultado directamente en la función original, ahora se tiene una función especializada que solamente se encarga de eso.

Esto también hace que el código sea más mantenible. Si en algún momento se necesita modificar la forma en que se imprime el resultado, solamente se tendría que modificar el decorador (en lugar de todas las funciones que lo utilizan).

>  
> 
> Los decoradores son una herramienta muy útil en Python para **mejorar la legibilidad y mantenibilidad del código**. Al separar la funcionalidad en diferentes funciones, se puede obtener un código más escalable y fácil de leer. Además, los decoradores hacen que el código sea más fácil de mantener, ya que las modificaciones se pueden realizar en un solo lugar.

