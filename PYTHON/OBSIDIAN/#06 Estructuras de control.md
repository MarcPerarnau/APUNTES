
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/estructuras-de-control-condicionales-y-bucles-en-python.webp)

## Estructuras de control en Python

Python, es un lenguaje de programación que se caracteriza por su simplicidad y facilidad de aprender. Sus estructuras de control nos permiten manipular la lógica de nuestros programas, facilitándonos la resolución de problemas.

Las **estructuras de control** son herramientas que nos permiten condicionar la ejecución del código a ciertas circunstancias. En Python, las estructuras de control más comunes son las **condicionales** y los **bucles**.

### Condicionales en Python

Los condicionales en python nos permiten **ejecutar una o varias instrucciones si se cumple una condición**. La estructura básica de un condicional en python es la siguiente:

```python
if condicion:
    instruccion
```

La **condición** es una expresión lógica que debe ser evaluada con el resultado de **verdadero** o **falso**. Si la condición se cumple, la **instrucción** se ejecutará.

Además de los **if**, también existe otras estructuras condicionales en Python que son:

#### if - else

La estructura **if - else** nos permite ejecutar una instrucción si se cumple la condición, y otra instrucción si no se cumple la condición.

```python
if condicion:
    instruccion1
else:
    instruccion2
```

#### if - elif - else

La estructura **if - elif - else** nos permite evaluar múltiples condiciones, ejecutando una instrucción diferente para cada una de ellas.

```python
if condicion1:
    instruccion1
elif condicion2:
    instruccion2
...
else:
    instruccionN
```

### Bucles en Python

Los bucles nos permiten repetir un conjunto de instrucciones varias veces, hasta que se cumpla una condición. En Python, existen dos tipos de bucles:

#### while

El bucle **while** se ejecuta mientras se cumpla una condición. La estructura básica es la siguiente:

```python
while condicion:
    instruccion
```

#### for

El bucle **for** nos permite iterar sobre una secuencia de elementos (listas, tuplas, diccionarios). La estructura básica es la siguiente:

```python
for elemento in secuencia:
    instruccion
```

### Ejemplos de uso

#### Condicionales

Imagine que va a un restaurante y el mesero le pregunta si desea una bebida caliente o fría. Podríamos utilizar una estructura condicional para tomar una decisión:

```python
bebida = input("¿Bebida caliente o fría?")
if bebida == "caliente":
    print("Servir té o café")
else:
    print("Servir refresco o agua")
```

#### Bucles

Imaginemos que queremos imprimir números del 1 al 5. Podríamos utilizar un bucle **for**:

```python
for numero in range(1,6):
    print(numero)
```

Otra tarea común es buscar un elemento específico en una lista. Podríamos utilizar un bucle **while**:

```python
lista = [1, 2, 3, 4, 5]
i = 0
encontrado = False
while i < len(lista) and not encontrado:
    if lista[i] == 3:
        print("Número encontrado en la posición:",i)
        encontrado = True
    i += 1
```

>[!TIP] TIP
> Las estructuras de control son fundamentales en Python para la resolución de problemas y una buena organización de nuestro código. Los condicionales y los bucles son herramientas poderosas que nos permiten automatizar tareas y tomar decisiones de manera eficiente. Es importante dominar estas estructuras para poder escribir programas más sofisticados y complejos.

## La importancia de las condiciones en la programación

Cuando estamos aprendiendo a programar en Python, uno de los conceptos fundamentales que tenemos que entender son las estructuras de control. **Las estructuras de control nos permiten hacer que un programa tome distintos caminos dependiendo de ciertas condiciones que se cumplan o no se cumplan**.

En particular, las condiciones son una pieza clave en la programación, ya que nos permiten crear programas mucho más complejos y útiles. Las condiciones nos permiten tomar decisiones en nuestro código, y hacer que el programa se comporte de distintas formas según el contexto.

Por ejemplo, consideremos el siguiente código:

```python
x = 5

if x > 10:
    print("x es mayor que 10")
else:
    print("x es menor o igual a 10")
```

En este código estamos usando una estructura condicional para determinar si el valor de `x` es mayor que 10 o no. Si el valor de `x` es mayor que 10, se va a imprimir “x es mayor que 10”. Si no es así, se imprimirá “x es menor o igual a 10”.

Notemos que esta condición nos permite hacer que el programa tome distintos caminos dependiendo del valor de `x`. Esto es muy útil en muchos contextos. Por ejemplo, si estamos escribiendo un programa que debe tomar decisiones automáticas en función de ciertos datos de entrada, las condiciones nos permiten hacer que el programa tome la mejor decisión en cada caso.

Otro ejemplo de la importancia de las condiciones es el siguiente:

```python
edad = int(input("Ingrese su edad: "))

if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")
```

En este caso, estamos usando una condición para determinar si el usuario es mayor de edad o no, en función de la edad que ha ingresado. Si el usuario tiene 18 años o más, el programa imprimirá “Eres mayor de edad”. De lo contrario, imprimirá “Eres menor de edad”.

Esta condición es importante porque nos permite hacer que el programa tome distintas decisiones en función de un dato importante: la edad del usuario. Si estuviéramos escribiendo un programa más complejo, podríamos usar esta información para tomar decisiones más elaboradas, como desplegar cierta información o realizar ciertas acciones en función de si el usuario es mayor o menor de edad.

> [!TIP] TIP
> Las condiciones son una parte fundamental de la programación en Python. Nos permiten hacer que nuestros programas tomen distintos caminos dependiendo de ciertos datos o situaciones, lo cual es muy útil en muchos contextos. Es importante que comprendamos bien el funcionamiento de las condiciones para poder crear programas más complejos y útiles.

## Cómo utilizar los condicionales en Python

Los condicionales son una estructura de control muy útil en Python que nos permiten tomar decisiones basadas en el valor de una expresión. En otras palabras, los condicionales nos permiten hacer que nuestro programa haga diferentes cosas dependiendo de si se cumple o no una cierta condición.

En Python, los condicionales se definen utilizando la palabra clave `if`, seguida por una expresión que debe ser evaluada como Verdadera o Falsa. Si la expresión es Verdadera, entonces se ejecutará el bloque de código indentado que viene después del `if`. Si la expresión es Falsa, entonces se saltará el bloque de código y se continuará con la ejecución normal del programa.

Veamos un ejemplo sencillo:

```python
edad = 20
if edad >= 18:
    print("Eres mayor de edad.")
```

En este ejemplo, la expresión que se evalúa es `edad >= 18`, que es Verdadera ya que la variable `edad` tiene el valor de `20`, que es mayor o igual a `18`. Como resultado, se imprimirá el mensaje `"Eres mayor de edad."`.

Si queremos que se haga algo diferente en caso de que no se cumpla la condición, podemos utilizar la palabra clave `else`. En este caso, si la expresión después del `if` es Falsa, se ejecutará el bloque de código después del `else`.

Veamos un ejemplo:

```python
edad = 16
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

En este ejemplo, la expresión `edad >= 18` es Falsa ya que `edad` es igual a `16`. Como resultado, se ejecutará el bloque de código después del `else`, que imprime el mensaje `"Eres menor de edad."`.

Por último, podemos utilizar la palabra clave `elif` para evaluar múltiples condiciones. En este caso, sólo se ejecutará el bloque de código correspondiente a la primera condición que sea Verdadera. Si ninguna condición es Verdadera, entonces se ejecutarán las líneas después del último `else` que se encuentre presente.

Veamos un ejemplo:

```python
nota = 7
if nota >= 9:
    print("Excelente.")
elif nota >= 7:
    print("Muy bien.")
elif nota >= 5:
    print("Regular.")
else:
    print("Reprobado.")
```

En este ejemplo, se evalúan varias condiciones para determinar la calificación correspondiente a una nota. Si la nota es mayor o igual a `9`, se imprime el mensaje `"Excelente."`. Si no, se evalúa la siguiente condición. En este caso, si la nota es mayor o igual a `7`, se imprime el mensaje `"Muy bien."`. Si no, se evalúa la siguiente condición. Finalmente, si la nota es mayor o igual a `5`, se imprime el mensaje `"Regular."`. Si ninguna de las condiciones anteriores se cumple, se imprime el mensaje `"Reprobado."`.

>[!TIP] TIP
> Los condicionales son una estructura de control muy útil en Python que nos permiten tomar decisiones basadas en el valor de una expresión. Con los condicionales `if`, `else` y `elif`, podemos hacer que nuestro programa haga diferentes cosas dependiendo de las condiciones que se cumplan.

## Bucles for y while en Python

Cuando hablamos de bucles en programación, nos referimos a una estructura que nos permite repetir una acción múltiples veces. En Python contamos con dos tipos de bucles: `for` y `while`.

### Bucle for

El bucle `for` nos permite repetir una acción un número definido de veces. Esto lo logramos utilizando un objeto iterable (como por ejemplo una lista) y luego realizar una acción para cada elemento dentro del objeto. La sintaxis básica es la siguiente:

```python
for variable in objeto_iterable:
    # acción que se debe repetir
```

Donde `variable` es la variable que utilizaremos para acceder a cada elemento dentro del objeto iterable. Por ejemplo:

```python
numeros = [1, 2, 3, 4, 5]
for num in numeros:
    print(num)
```

Este código imprimirá los números del 1 al 5 en la consola.

### Bucle while

El bucle `while` nos permite repetir una acción mientras se cumpla una condición. Esto lo logramos utilizando una expresión que evaula a `True` o `False` como la condición. La sintaxis básica es la siguiente:

```python
while condicion:
    # acción que se debe repetir
```

Donde `condicion` es la expresión que estamos evaluando. Por ejemplo:

```python
cantidad = 0
while cantidad < 10:
    print(cantidad)
    cantidad += 1
```

Este código imprimirá los números del 0 al 9 en la consola. La variable `cantidad` comienza en 0 y se va incrementando en 1 hasta que llega a ser mayor o igual a 10, lo que hace que se deje de cumplir la condición.

### Ejemplos de uso

Podemos utilizar los bucles for y while para realizar varias operaciones repetidas veces, como por ejemplo imprimir la tabla del 2:

```python
for i in range(1, 11):
    print("2 x", i, "=", 2 * i)
```

Este código imprimirá la tabla del 2, multiplicando cada número del 1 al 10 por 2.

```python
numero = 1
while numero <= 100:
    if numero % 3 == 0 and numero % 5 == 0:
        print("FizzBuzz")
    elif numero % 3 == 0:
        print("Fizz")
    elif numero % 5 == 0:
        print("Buzz")
    else:
        print(numero)
    numero += 1
```

Este código imprimirá los números del 1 al 100, pero si un número es divisible por 3 imprimirá “Fizz”, si es divisible por 5 imprimirá “Buzz” y si es divisible por ambos imprimirá “FizzBuzz”.

> [!TIP] TIP
> Los bucles for y while son herramientas poderosas para repetir acciones en Python. Es importante tener en cuenta que debemos cuidar de no caer en bucles infinitos, es decir, bucles que nunca se detienen debido a que la condición nunca se deja de cumplir.

## Iterando sobre elementos de una lista con for

Uno de los usos más comunes de los bucles en Python es iterar sobre una lista de elementos. En otras palabras, recorremos una lista de elementos uno a uno e hicimos algo con cada uno de ellos.

La sintaxis más común para esto es utilizar un bucle for junto con la función len () para obtener la longitud de la lista. Luego, utilizamos el operador de rango para obtener un rango de índices, que luego utilizamos para acceder a cada elemento de la lista.

```python
    lista = ['Manzana', 'Pera', 'Plátano', 'Fresa']

    for i in range(len(lista)):
        print(lista[i])
```

En este ejemplo, las palabras `Manzana`, `Pera`, `Plátano` y `Fresa` corresponden a los elementos de nuestra lista. El bucle for itera sobre ellos y los imprime uno por uno en la pantalla.

Otra forma de hacer esto es utilizando el bucle for directamente sobre la lista. Este enfoque es más limpio y directo y generalmente se considera la forma “más pythonica” de iterar sobre una lista de elementos.

```python
    lista = ['Manzana', 'Pera', 'Plátano', 'Fresa']

    for elemento in lista:
        print(elemento)
```

Este código produce la misma salida que el anterior.

Es importante tener en cuenta que, al iterar sobre una lista de esta manera, no tenemos acceso a los índices de los elementos de la lista. Sin embargo, a menudo no necesitamos el índice y simplemente queremos hacer algo con cada elemento de la lista.

Otro beneficio de iterar sobre una lista de esta manera es que podemos utilizar la función `enumerate()` para obtener tanto el índice como el valor del elemento en cada iteración.

```python
    lista = ['Manzana', 'Pera', 'Plátano', 'Fresa']

    for i, elemento in enumerate(lista):
        print(i, elemento)
```

Este código produce la salida:

```python
    0 Manzana
    1 Pera
    2 Plátano
    3 Fresa
```

Al utilizar `enumerate()` con el bucle for, obtenemos tanto el índice del elemento actual como el valor de ese elemento. De esta forma podemos personalizar la salida para que muestre el índice correspondiente a cada elemento de la lista.

> [!TIP] TIP
> Al trabajar con estructuras de control en Python, iterar sobre elementos de una lista con el bucle `for` es una práctica muy común. Al utilizar la sintaxis adecuada, podemos recorrer la lista de una manera clara y concisa, y personalizar la salida según nuestras necesidades.

## Cómo evitar loops infinitos en Python

Cuando se programa, es común encontrarse con situaciones en las que un loop debería finalizar después de un cierto número de iteraciones, pero por alguna razón no lo hace y se queda en un ciclo inifinito. Esto se conoce como un **loop infinito** y puede causar estragos en el rendimiento de nuestro código. En Python, hay varias formas de evitar loops infinitos. Aquí les mostramos algunas estrategias que hemos encontrado útiles:

## 1. Usar una condición de salida

En lugar de confiar en una variable en el loop para terminarlo, es aconsejable usar una condición de salida. Nuestro loop debería continuar mientras la condición sea True, pero si la condición se cumple, deberíamos salir del loop en lugar de esperar que una variable cambie. Aquí hay un ejemplo:

```python
x = 0
while True:
    print(x)
    x += 1
    if x > 10:
        break
```

En este ejemplo, la condición que detiene el loop es que x sea mayor que 10. Una vez que esa condición se cumple, salimos del loop usando la palabra clave `break`.

## 2. Usar un contador

Otra manera de evitar loops infinitos es usar un contador. En lugar de confiar en una variable para cambiar de valor, podemos usar un contador para contar el número de iteraciones que se han realizado y detener el loop cuando llega a un número específico. Aquí hay un ejemplo:

```python
counter = 0
while counter < 10:
    print(counter)
    counter += 1
```

En este ejemplo, el loop continuará hasta que el contador alcance un valor de 10. En ese punto, el loop se detendrá y el código continuará ejecutándose después del loop.

## 3. Usar un sleep timer

Si sospechamos que nuestro loop no está funcionando correctamente y estamos preocupados por un loop infinito, podemos agregar un temporizador de espera al loop. Un temporizador de espera hará que la ejecución se detenga por un periodo de tiempo determinado, lo que nos permitirá verificar si el loop se está ejecutando correctamente o no. Aquí está el código:

```python
import time

while True:
    print("El loop está funcionando.")
    time.sleep(1) # esto hará que la ejecución se detenga por 1 segundo
```

En este ejemplo, agregamos un temporizador de espera que detendrá la ejecución del loop por 1 segundo cada vez que se complete una iteración.

> [!TIP] TIP
> Con estas tres estrategias probadas y verdaderas, ahora podemos evitar fácilmente loops infinitos en Python y mantener nuestro código funcionando en continuo progreso. Recuerda siempre usar una estrategia de detención en tu loop para mantener el control y evitar errores innecesarios en tus programas.

## El uso de break y continue en bucles

En Python, los bucles son una estructura de control fundamental que nos permiten repetir una acción tantas veces como sea necesario. A menudo, necesitamos modificar el flujo de un bucle en función de ciertas condiciones. En este caso, las funciones `break` continue` son muy útiles.

La función `break` se utiliza en un bucle para detener la iteración inmediatamente y salir del bucle. Por ejemplo, supongamos que queremos buscar un valor específico en una lista y queremos salir del bucle tan pronto como lo encontremos:

```python
my_list = [1, 2, 3, 4, 5]

for num in my_list:
  if num == 3:
    print("Encontrado.")
    break
  print(num)

# Salida:
# 1
# 2
# Encontrado.
```

En el ejemplo anterior, el bucle `for` recorre los números en la lista `my_list`. Cuando el valor `3` se encuentra, imprime “Encontrado” y usa la función `break` para salir del bucle inmediatamente. Como resultado, solo se imprimieron los valores `1` y `2`.

Por otro lado, la función `continue` se utiliza para saltar una iteración y continuar con la siguiente, sin ejecutar el código que queda de la iteración actual. Por ejemplo, si queremos imprimir todos los números en la lista excepto el número `3`, podemos usar la función `continue` para saltar ese número:

```python
my_list = [1, 2, 3, 4, 5]

for num in my_list:
  if num == 3:
    continue
  print(num)

# Salida:
# 1
# 2
# 4
# 5
```

En este ejemplo, cuando el valor `3` en la lista es evaluado en la condición `if`, el código restante de la iteración actual es saltado y la siguiente iteración comienza con el siguiente valor en la lista.

Tanto `break` como `continue` son herramientas útiles para controlar el flujo de los bucles en Python, pero también es importante tener en cuenta su uso adecuado para evitar errores y asegurarnos que el codigo sea comprensible para otros programadores.

> [!TIP] TIP
> `break` se utiliza para detener la iteración inmediatamente y salir del bucle, mientras que `continue` se utiliza para saltar una iteración y continuar con la siguiente. Recordemos utilizar estas herramientas de manera adecuada y responsable para simplificar nuestros bucles.

## Optimización y eficiencia en el uso de estructuras de control

La **optimización y eficiencia en el uso de estructuras de control** es un tema muy importante en el aprendizaje de Python. Cuando comencé a aprender a programar, me encontré con la necesidad de entender cómo funcionaban las estructuras de control en Python, especialmente los condicionales y los bucles. Pero no fue hasta que empecé a trabajar en proyectos más grandes que me di cuenta de la importancia de optimizar y hacer más eficiente el uso de estas estructuras.

Una de las formas más comunes de optimización es **utilizar un bucle for en lugar de un bucle while**, ya que en la mayoría de los casos es más fácil de leer y puede ahorrar tiempo de escritura de código. Además, el uso de la función range permite crear bucles con un número predeterminado de iteraciones, lo que ayuda a simplificar el código y reducir errores.

Otra forma de optimizar el uso de estructuras de control es **evitar la repetición de código innecesario**. Por ejemplo, en lugar de escribir múltiples condicionales if-else o nested if-else, se puede usar una estructura de control switch. Aunque Python no tiene una estructura de control switch incorporada, se puede emular usando un diccionario o una serie de funciones.

Además, es importante tener en cuenta la **eficiencia en términos de tiempo de ejecución del código**. Por ejemplo, si se va a recorrer una lista o un archivo grande varias veces, es más eficiente leerlo en memoria una sola vez y guardar los valores en una variable o array para usarlos en el bucle.

También es importante evitar el **uso de condicionales dentro de un bucle en la medida de lo posible**, ya que las iteraciones implican un costo de tiempo y recursos. En su lugar, se puede preprocesar o filtrar los datos antes de entrar al bucle.

Un buen hábito para optimizar el uso de bucles es **definir variables fuera del loop, y solo actualizarlas dentro del mismo**. Si se define una variable en cada iteración, el programa se ralentiza y consume más recursos.

>[!TIP] TIP
> La optimización y eficiencia en el uso de estructuras de control es un tema vital cuando se trata de escribir código Python efectivo y rápido. Al utilizar técnicas de simplificación de código, bucle for, switch, filtrado de datos y definir variables fuera del bucle, podemos lograr un código más legible, mantenible y escalable, al mismo tiempo que se mejora la eficiencia y el tiempo de ejecución del código.

## Errores comunes al utilizar condicionales y bucles en Python

En nuestro proceso de aprendizaje Python nos encontramos con un universo de posibilidades y herramientas para desarrollar código de manera eficiente y efectiva. Y dentro de las herramientas más importantes están las estructuras de control como son las condicionales y los bucles. Es importante mencionar que cuando iniciamos en este lenguaje de programación es fácil cometer errores comunes al utilizar estas estructuras, pero no debemos desanimarnos, con práctica y dedicación podemos superar estos obstáculos. A continuación, mencionaremos algunos de los errores más comunes que hemos experimentado y cómo los solucionamos:

1. Indentación incorrecta en las estructuras de control
    La indentación es fundamental en Python, ya que no existe un delimitador de bloque como lo hemos visto en otros lenguajes de programación. En ocasiones podemos tener una indentación incorrecta en algún trozo de código y empezar a tener problemas con la ejecución del mismo. Recuerda que la indentación en Python se realiza con **4 espacios** o con **1 Tabulador**.
    
    ```python
    if x > 5:
    print("El valor de x es mayor que 5")
    ```
    
    La corrección de este error sería agregar cuatro espacios antes de nuestra sentencia print() para que el condicional pueda ser ejecutado correctamente.
    
    ```python
    if x > 5:
        print("El valor de x es mayor que 5")
    ```
    
2. Uso incorrecto de operadores lógicos en las condicionales
    Existen tres operadores lógicos en Python: **and**, **or** y **not**, se utilizan para comparar dos o más condiciones. Al trabajar con más de una expresión lógica, es importante utilizarlos adecuadamente para evitar comportamientos inesperados.
    
    ```python
    if x > 5 and x < 10 or x == 20:
        print("El valor de x está dentro del rango")
    ```
    
    En este ejemplo, tenemos una condicional que debe imprimir un mensaje si el valor de **x** está entre 5 y 10, o si es igual a 20. Pero el operador lógico **or** no funciona como se espera, ya que se pregunta primero si x es mayor que 5 y menor que 10, y si esto no se cumple, entonces evalúa si **x==20**. Una solución sería agrupar las expresiones dentro de los paréntesis para que la jerarquía se aplique correctamente.
    
    ```python
    if (x > 5 and x < 10) or x == 20:
        print("El valor de x está dentro del rango")
    ```
    
3. Bucles infinitos
	Al utilizar bucles en nuestro código, es común caer en bucles infinitos, los cuales nos dejan nuestro programa “colgado” sin respuesta. Esto puede suceder si no especificamos correctamente la condición de salida en nuestro bucle.
    
    ```python
    while x < 5:
        print("Hola")
    ```
    
    En este ejemplo, **x** no se incrementa nunca dentro del bucle, lo que hace que la condición **x < 5** siempre se cumpla. Para corregirlo, necesitamos especificar una forma de salida del bucle, por ejemplo, podemos incrementar **x** dentro de nuestro bucle mientras se cumpla la condición.
    
    ```python
    while x < 5:
        print("Hola")
        x += 1
    ```
    

> [!TIP] TIP
> Para evitar cometer errores comunes al utilizar condicionales y bucles en Python, es importante prestar atención al uso correcto de la indentación, los operadores lógicos y la condición de salida en nuestros bucles. Con la práctica y la dedicación, podremos construir programas más robustos y eficientes utilizando estas herramientas
