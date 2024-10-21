
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/excepciones-en-python-manejo-de-errores-sin-complicaciones.webp)

## Manejo de errores en Python es fundamental para cualquier programador

Si hay algo que debes saber como programador de Python es cómo **manejar errores**. Es fundamental para poder desarrollar programas con éxito. Quizás pienses que es algo que solo se aprende con la experiencia, pero en realidad es algo que deberías saber desde el primer día.

El error es algo común en la programación, y en Python hay muchas formas de manejar estos errores. Como programadores, debemos ser capaces de manejar cualquier error que se presente en el programa. Si no sabemos manejar los errores, nuestro programa puede fallar sin explicación.

¿Pero cómo manejar los errores en Python? La respuesta es bastante sencilla: ¡con excepciones! Las excepciones son objetos que se utilizan para manejar errores, y es la forma más eficaz y elegante de manejar errores en Python.

Un error común en Python es el **NameError**, que se produce cuando se utiliza una variable que no ha sido definida. Si intentamos ejecutar el siguiente código, obtendremos un error:

```py
print(variable)
```

Este código produce un **NameError** porque la variable no ha sido definida. Para evitar este error, podemos utilizar una excepción:

```py
try:
    print(variable)
except NameError:
    print("La variable no ha sido definida")
```

Este código intenta imprimir la variable, pero si se produce un **NameError**, el código dentro del bloque `except` se ejecutará, en este caso, imprimirá un mensaje indicando que la variable no ha sido definida.

Otro error común es el **TypeError**, que se produce cuando intentamos realizar una operación con un objeto de un tipo incorrecto. Si intentamos sumar un número con una cadena de texto, obtendremos un **TypeError**:

```py
numero = 5
texto = "Hola mundo"
resultado = numero + texto
print(resultado)
```

Este código produce un **TypeError** porque estamos tratando de sumar dos tipos de datos que no son compatibles. Para evitar este error, podemos utilizar una excepción:

```py
numero = 5
texto = "Hola mundo"
try:
    resultado = numero + texto
except TypeError:
    print("No se puede sumar un número con una cadena de texto")
```

Este código intenta sumar el número y la cadena de texto, pero si se produce un **TypeError**, el código dentro del bloque `except` se ejecutará, en este caso, imprimirá un mensaje indicando que no se pueden sumar ambos tipos de datos.

>  
> 
> Manejar errores en Python es fácil y esencial para cualquier programador. Las excepciones te permiten manejar los errores de manera elegante y evitar que tu programa se vuelva inestable o incluso fallido. ¡Así que no lo dudes, aprende a manejar excepciones en Python desde hoy mismo!

## Excepciones en Python permiten manejar errores de manera efectiva

Al programar en cualquier lenguaje, siempre es importante tomar en cuenta que los errores pueden aparecer en cualquier momento. Por esta razón, es vital contar con un buen manejo de excepciones que permita detectar y corregir los problemas que puedan surgir.

En Python, el **manejo de excepciones** es una funcionalidad muy poderosa que permite detectar y controlar errores en los programas de manera segura y eficiente. La sintaxis de este lenguaje permite la detección de cualquier tipo de error, desde los más simples hasta los más complejos.

El manejo de excepciones se lleva a cabo dentro de bloques de código que están identificados por la palabra clave “try”. Dentro de ese bloque de código se pueden escribir instrucciones que se espera que sean ejecutadas sin errores. En caso de que alguno de estos produzca una excepción, se puede manejar el error dentro de un bloque “except”.

Por ejemplo, imaginemos que estamos desarrollando un programa que hace alguna operación matemática con números ingresados por el usuario. Si el usuario ingresa un valor no numérico, se produciría una excepción que rompería el flujo normal del programa. Es aquí donde entra en juego el manejo de excepciones.

```py
try:
    num1 = input("Ingresa un número: ")
    num2 = input("Ingresa otro número: ")
    resultado = int(num1) + int(num2)
    print(f"La suma de {num1} y {num2} es {resultado}")
except ValueError:
    print("Uno de los valores ingresados no es numérico")
```

En este ejemplo, el bloque “try” intenta sumar los valores ingresados por el usuario y mostrar el resultado en pantalla. Si alguno de los valores no es numérico, se produciría una excepción del tipo “ValueError”. Es por eso que el bloque “except” específica ese tipo de excepción para manejar el error y mostrar un mensaje de ayuda al usuario.

Cabe destacar que en Python también se pueden crear excepciones personalizadas mediante la creación de nuevas clases. Esta funcionalidad permite crear excepciones específicas para los programas en los que estemos trabajando.

>  
> 
> El manejo de excepciones en Python es una característica vital que permite controlar errores de manera eficaz. Con la sintaxis clara y fácil de usar de este lenguaje, el manejo de excepciones se convierte en una herramienta poderosa para el desarrollo de aplicaciones confiables y seguras.

## Conociendo los tipos de excepciones es esencial para manejar errores

Cuando empecé a aprender Python, una de las cosas que más me costó entender fue **cómo manejar errores**. A menudo, cuando intentaba ejecutar mi código, aparecían mensajes de error que no entendía. Pero luego descubrí que estos mensajes eran muy útiles para identificar lo que estaba mal en mi código y para corregirlo.

Una de las cosas más importantes que aprendí fue sobre los **tipos de excepciones**. En Python, una excepción es un evento que interrumpe la ejecución normal de un programa y se produce cuando se encuentra un error. Cada tipo de error tiene su propia excepción. Conociendo los tipos de excepciones, pude entender mejor mis errores y por lo tanto manejarlos más fácilmente.

Por ejemplo, si intentamos dividir un número por cero, Python lanzará una excepción del tipo ZeroDivisionError. Si tratamos de abrir un archivo que no existe, Python lanzará una excepción del tipo FileNotFoundError. Si intentamos acceder a un elemento de una lista o diccionario que no existe, Python lanzará una excepción del tipo KeyError.

Aquí hay algunos ejemplos de cómo manejar estas excepciones:

```py
# Manejando una excepción ZeroDivisionError
try:
    resultado = 10/0
except ZeroDivisionError:
    print("No se puede dividir un número por cero")

# Manejando una excepción FileNotFoundError
try:
    archivo = open("archivo_que_no_existe.txt")
except FileNotFoundError:
    print("No se puede abrir el archivo porque no existe")

# Manejando una excepción KeyError
mi_diccionario = {"llave1": "valor1", "llave2": "valor2"}
try:
    valor = mi_diccionario["llave3"]
except KeyError:
    print("La llave no existe en el diccionario")
```

En estos ejemplos, utilizamos el bloque `try-except` para manejar las excepciones. El código dentro del bloque `try` es el que podría generar una excepción. Si se produce una excepción, el código dentro del bloque `except` se ejecutará en su lugar. De esta manera, podemos prevenir que nuestro programa se detenga abruptamente y en su lugar dar una respuesta elegante al error.

>  
> 
> Conociendo los tipos de excepciones y cómo manejarlas, podemos hacer que nuestro código sea más robusto y resistente a errores. Así que, si eres nuevo en Python, asegúrate de pasar algún tiempo familiarizándote con las excepciones y cómo manejarlas. ¡Te ahorrarán muchas horas de frustración!

## Cómo personalizar excepciones y mejorar la legibilidad de nuestro código

Cuando se manejan excepciones en Python, a veces es útil personalizarlas para construir un manejo de errores más comprensible. Python nos permite crear nuestras propias excepciones para que podamos proporcionar información relevante y significativa para el manejo de errores de nuestros programas.

Si bien es posible manejar excepciones sin definir nuestras propias excepciones personalizadas, esto puede hacer más difícil descubrir qué salió mal en su código. Esto puede volverse especialmente difícil cuando trabajamos con una base de código grande y compleja. Con personalizar nuestras excepciones, mejoramos la legibilidad y mantenibilidad de nuestro código.

Para crear una excepción personalizada, necesitamos crear una clase que herede de la clase “Exception”. Esto se puede ver en el siguiente ejemplo:

```py
class MiErrorPersonalizado(Exception):
    pass
```

Aquí hemos definido una nueva clase llamada `MiErrorPersonalizado` que hereda de la clase “Exception”. Esta clase no tiene definida ninguna funcionalidad adicional, pero puede usarse como una excepción en nuestro código.

Una vez que hemos definido nuestra excepción personalizada, podemos levantarla en nuestro código cuando surja una situación particular. El siguiente ejemplo muestra como levantar la excepción personalizada `MiErrorPersonalizado`.

```py
def mi_funcion():
    raise MiErrorPersonalizado("Ocurrio un error personalizado")
```

En este ejemplo, hemos definido una función llamada `mi_funcion` que contiene el `raise` statement. Al llamar a esta función se levantará la excepción `MiErrorPersonalizado` junto con un mensaje específico.

Igual que las excepciones incorporadas en Python, las excepciones personalizadas pueden tener argumentos opcionales para proporcionar contexto adicional. El siguiente ejemplo muestra como definir una excepción personalizada con un argumento.

```py
class ValorInvalidoError(Exception):
    def __init__(self, mensaje, valor):
        super().__init__(mensaje)
        self.valor = valor
```

En este ejemplo, hemos definido una nueva excepción llamada `ValorInvalidoError` que hereda de la clase “Exception”. Hemos proporcionado un mensaje que describe el error, así como un argumento adicional llamado `valor` que almacena el valor que causó la excepción.

Podemos usar esta excepción personalizada en nuestro código de la siguiente manera:

```py
def mi_funcion(valor):
    if valor < 0:
        raise ValorInvalidoError("El valor no puede ser negativo", valor)
```

En este ejemplo, hemos definido una función llamada `mi_funcion` que levanta la excepción personalizada `ValorInvalidoError` si se pasa un valor negativo.

>  
> 
> Personalizar excepciones en Python puede hacer que sea más fácil manejar errores y mejorar la legibilidad de nuestro código. Al definir nuestras propias excepciones personalizadas, podemos proporcionar una información clara y concisa sobre por qué ocurrió un error y hacer que nuestro código sea más fácil de mantener.

## El uso del bloque finally para garantizar la ejecución de código importante

En la programación, es común encontrarnos con situaciones en las que se deben ejecutar tareas importantes de manera obligatoria, sin importar si ocurrió un error en el programa o si este terminó de manera exitosa. En estos casos, el bloque finally resulta de gran utilidad.

El bloque finally se utiliza en conjunto con los bloques try y except. En términos sencillos, el bloque try es utilizado para “intentar” ejecutar un conjunto de instrucciones, mientras que el bloque except se encarga de “atrapar” cualquier excepción o error que pueda ocurrir durante la ejecución del bloque try.

El bloque finally, por otro lado, se usa para ejecutar código que es importante y necesitamos que se ejecute sin importar si hubo un error o no en la ejecución del código anterior.

Veamos un ejemplo sencillo:

```py
try:
    x = 5 / 0
except ZeroDivisionError:
    print("No puedes dividir entre cero.")
finally:
    print("Este código se ejecutará sin importar si se produjo una excepción o no.")
```

En este ejemplo, se intenta dividir el número 5 entre 0, lo cual produce una excepción de ZeroDivisionError. La excepción es “atrapada” por el bloque except, que imprime un mensaje en la consola. Finalmente, el bloque finally se ejecuta, imprimiendo otro mensaje en la consola.

Es importante mencionar que **el bloque finally se ejecutará incluso si ocurre un error diferente al que se “atrapó” en el bloque except**. Por ejemplo:

```py
try:
    x = 5 / 0
except ValueError:
    print("No puedes dividir entre cero.")
finally:
    print("Este código se ejecutará sin importar si se produjo una excepción o no.")
```

En este ejemplo, se espera “atrapar” una excepción de ValueError, pero como la excepción que realmente ocurre es de ZeroDivisionError, el bloque except no se ejecutará, pero el bloque finally sí.

>  
> 
> El bloque finally es una herramienta esencial para garantizar que cierto código importante se ejecutará sin importar qué ocurre durante la ejecución del resto del programa. Su uso es sencillo y se combina con los bloques try y except para manejar excepciones y errores en Python.