
![](https://img.am80.com/?width=1024&url=https://assets.apuntes.de/headers/python/variables-y-tipos-de-datos-en-python.webp)

## ¿Qué es una variable?

Cuando aprendemos a programar en Python, una de las primeras cosas que debemos entender son las **variables**. En esencia, una variable es un espacio de memoria reservado en nuestro programa para almacenar un valor. Este valor puede ser un número, una cadena de texto, un objeto, entre otros.

En Python, las variables se crean al darles un nombre y asignarles un valor. Por ejemplo, si queremos crear una variable llamada “edad” que almacene un valor de 25, podemos escribir:

```python
edad = 25
```

Ahora, podemos utilizar esta variable en nuestro programa. Por ejemplo, podríamos imprimir el valor de la variable en la consola utilizando la función “print”:

```python
print(edad) # imprimirá 25
```

Más adelante, si queremos cambiar el valor almacenado en nuestra variable “edad”, podemos hacerlo simplemente asignándole un nuevo valor:

```python
edad = 30
```

Ahora, al imprimir el valor de “edad” nuevamente, veremos que ha cambiado:

```python
print(edad) # imprimirá 30
```

Es importante tener en cuenta que en Python, las variables son **dinámicas**, lo que significa que no necesitamos especificar de antemano qué tipo de valor almacenarán. Por ejemplo, podríamos crear una variable llamada “nombre” que almacena una cadena de texto:

```python
nombre = "Juan"
```

Y luego, cambiarla a almacenar un número:

```python
nombre = 33
```

Aunque esta flexibilidad puede ser conveniente, también puede hacer que el código sea más difícil de leer y mantener. Para ayudar a mitigar esto, es útil seguir buenas prácticas de programación, como nombrar las variables de manera descriptiva y utilizar comentarios para explicar su propósito.

> [!TIP] TIP
> **Una variable es un espacio de memoria reservado** para almacenar un valor en nuestro programa en Python. Podemos asignarles valores y utilizarlas en nuestro código, y su flexibilidad dinámica nos da una gran libertad, pero también requiere de disciplina y organización para asegurarnos de que nuestro código sea legible y mantenible.

## ¿Cómo definir y asignar variables en Pyton?

En Python, **las variables se definen y se asignan valores** utilizando el símbolo “=”.

Para definir una variable, simplemente debemos pensar un nombre para ella. En mi experiencia, elegir nombres claros y descriptivos simplifica la tarea de escribir código. Por ejemplo, si estoy escribiendo un programa que calcula la suma de dos números, podría definir dos variables para guardar esos números:

```python
numero1 = 5
numero2 = 7
```

En este caso, he definido dos variables llamadas “numero1” y “numero2”. Les he asignado los valores 5 y 7, respectivamente.

Es importante destacar que, en Python, **las variables no necesitan ser declaradas antes de ser utilizadas**. Simplemente basta con definirlas y asignarles un valor.

Una vez que hemos definido nuestras variables, podemos utilizarlas para hacer operaciones. Por ejemplo, si queremos calcular la suma de los valores de las variables “numero1” y “numero2”, podemos hacer lo siguiente:

```python
suma = numero1 + numero2
print(suma)
```

En este caso, he definido una nueva variable llamada “suma”, la cual guarda el resultado de la operación “numero1 + numero2”. Luego, he utilizado la función “print()” para imprimir el valor de la variable “suma” en la consola.

Es importante destacar que, en Python, **el tipo de dato de una variable se infiere automáticamente**. Esto significa que no es necesario especificar el tipo de dato al definir una variable. Por ejemplo, si definimos una variable y le asignamos un valor entero, Python automáticamente la considerará como un tipo de dato entero (int). En cambio, si le asignamos un valor decimal, la considerará como un tipo de dato flotante (float).

Veamos un ejemplo:

```python
entero = 5
decimal = 3.14

print(type(entero))   # int
print(type(decimal))  # float
```

En este caso, he definido dos variables: una variable “entero”, a la que le he asignado el valor 5 (un número entero), y una variable “decimal”, a la que le he asignado el valor 3.14 (un número decimal). Luego, he utilizado la función “type()” para imprimir el tipo de dato de cada variable en la consola.

> [!TIP] TIP
> En Python podemos **definir y asignar valores a variables** de manera sencilla y rápida utilizando el símbolo “=”. No es necesario declarar las variables antes de utilizarlas, y el tipo de dato de una variable se infiere automáticamente. Es importante elegir nombres claros y descriptivos para nuestras variables, y utilizarlos para simplificar la tarea de escribir código.

## ¿Cómo funciona el scope en Python?

En Python, el **scope** es la región del programa en la que una variable es reconocida. Si intentas usar una variable fuera de su alcance, se produce un error. Es importante entender el scope de las variables en Python para evitar errores y escribir código más eficiente.

Hay dos tipos de scopes en Python: **global** y **local**. El scope global es el espacio de nombres que está disponible en todo el programa. Se puede acceder a él desde cualquier función o clase. Por otro lado, el scope local es el espacio de nombres que está disponible solo dentro de una función o clase. No se puede acceder a él desde fuera de la función o clase.

Una variable declarada dentro de una función o clase tiene un scope local. Si una variable tiene el mismo nombre que una variable global, la variable local oculta la global dentro del alcance de la función o clase. Por ejemplo:

```python
x = 5  # Variable global

def example():
    x = 10  # Variable local
    print(x)

example()  # Salida: 10
print(x)   # Salida: 5
```

En el ejemplo anterior, hay una variable global `x` con un valor de 5. La función `example()` define una variable local `x` con un valor de 10. Cuando la función se llama, imprime el valor de la variable local `x`, que es 10. Sin embargo, fuera de la función, la variable global `x` mantiene su valor de 5.

Si una variable se utiliza antes de ser asignada dentro de una función o clase, Python asume que es una variable global. Por lo tanto, si intentas asignar un valor a esta variable, se produce un error. Para evitar esto, se puede usar la palabra clave `global` para indicar que se está utilizando una variable global. Por ejemplo:

```python
x = 5  # Variable global

def example():
    global x
    x = 10
    print(x)

example()  # Salida: 10
print(x)   # Salida: 10
```

En el ejemplo anterior, la palabra clave `global` se utiliza para indicar que se está utilizando la variable global `x` dentro de la función. La función asigna un valor de 10 a `x`, que actualiza la variable global. Como resultado, las dos llamadas a `print()` producen el valor 10.

> [!TIP] TIP
> El scope en Python es importante para **definir variables de manera segura y eficiente**. Es útil saber cuándo se está utilizando una **variable global o local** y cómo se pueden evitar errores al actualizar variables globales dentro de funciones o clases. Con un conocimiento sólido del scope en Python, se pueden escribir programas más limpios y eficientes.

## ¿Cuáles son los tipos de datos en Python?

En Python, existen **diferentes tipos de datos** que son utilizados para realizar operaciones. Los tipos de datos son importantes ya que determinan la capacidad de almacenamiento, los tipos de operaciones a realizar y contribuyen a la correcta utilización de la memoria del equipo.

Los tipos de datos en Python incluyen:

### Números

En Python, **los números** son un tipo de dato importante y se utilizan para realizar operaciones matemáticas. Los números pueden ser enteros, plataformas flotantes y complejos. Los números enteros representan valores enteros, mientras que los plataformas flotantes representan números con decimales. Los números complejos representan números que tienen una parte real y una imaginaria.

```python
entero = 5
flotante = 2.5
complejo = 3 + 2j
```

### Cadenas de texto

**Las cadenas de texto** son un tipo de dato que es utilizado para representar texto y se encierran en comillas simples o dobles. Las cadenas de texto son inmutables, lo que significa que una vez que se ha creado una cadena de texto, no se puede modificar.

```python
nombre = "Juan"
mensaje = "Hola, bienvenido"
```

### Booleanos

**Los valores booleanos** se utilizan para representar verdadero o falso. Los valores booleanos son importantes en la toma de decisiones y en la evaluación de condiciones.

```python
verdadero = True
falso = False
```

### Listas

**Las listas** son un tipo de dato importante en Python que se utilizan para almacenar una colección de elementos. Los elementos de una lista pueden ser de diferentes tipos de datos. Las listas son mutables, lo que significa que se pueden agregar, eliminar y modificar elementos.

```python
lista_numeros = [1, 2, 3, 4, 5]
lista_palabras = ["hola", "adios", "bienvenido"]
```

### Tuplas

**Las tuplas** son similares a las listas, pero son inmutables, lo que significa que una vez que se han creado, no se pueden modificar. Las tuplas se utilizan para almacenar elementos que no cambiarán durante la ejecución del programa.

```python
tupla_numeros = (1, 2, 3, 4, 5)
tupla_palabras = ("hola", "adios", "bienvenido")
```

### Conjuntos

**Los conjuntos** son un tipo de dato que se utiliza para almacenar elementos únicos y no ordenados. Los elementos en un conjunto no pueden repetirse y se utilizan para realizar operaciones matemáticas como la unión, intersección y diferencia.

```python
conjunto_numeros = {1, 2, 3, 4, 5}
conjunto_letras = {"a", "b", "c", "d"}
```

### Diccionarios

**Los diccionarios** son un tipo de dato importante en Python que se utilizan para almacenar pares de clave-valor. Las claves se utilizan para indexar y recuperar valores. Los diccionarios son mutables y se pueden actualizar agregando y eliminando pares clave-valor.

```python
diccionario = {"nombre": "Juan", "edad": 25, "direccion": "Calle 10 #20-30"}
```

>[!TIP] TIP
> En Python, hay muchos **tipos de datos** para trabajar. Al comprender los diferentes tipos de datos disponibles, es posible realizar operaciones exitosas y optimizar la memoria del equipo. Los tipos de datos son una parte importante del lenguaje de programación Python y son esenciales para el éxito en la programación.

## ¿Cómo convertir entre tipos de datos en Python?

En Python, es común tener que **convertir entre diferentes tipos de datos**, y puede ser una tarea un poco tediosa en algunos casos. Sin embargo, es importante estar familiarizado con este proceso ya que es muy útil en la programación diaria.

Una forma común de convertir entre tipos de datos en Python es mediante **la función “casting”**. Esto implica tomar un valor de un tipo de datos y convertirlo en otro tipo de datos. Por ejemplo, si necesitamos tomar un número entero y convertirlo en una cadena, podemos usar la función “str()”, que convierte el valor en una cadena de caracteres. Veamos un ejemplo simple:

```python
numero_entero = 42
cadena_de_texto = str(numero_entero)
```

En este caso, la variable “cadena_de_texto” contendrá el valor “42” en forma de una cadena de caracteres. También podemos hacer lo mismo para convertir una cadena de caracteres en un número entero:

```python
cadena_de_texto = "42"
numero_entero = int(cadena_de_texto)
```

En este caso, la variable “numero_entero” contendrá el valor 42 en forma de un número entero. También es posible convertir números de punto flotante en números enteros mediante la función “int()”. En este caso, Python simplemente truncará el valor decimal y devolverá el número entero correspondiente:

```python
numero_flotante = 3.14159
numero_entero = int(numero_flotante)
```

En este caso, la variable “numero_entero” contendrá el valor 3, que es la versión truncada del número flotante original.

En algunos casos, puede ser útil convertir una cadena de caracteres en una lista. Este proceso implica tomar la cadena original y separarla en elementos separados por un delimitador específico. Por ejemplo, si tenemos una cadena que contiene una lista de números separados por comas, podemos convertirla en una lista de números enteros de la siguiente manera:

```python
cadena_de_texto = "1,2,3,4,5"
lista_de_numeros = cadena_de_texto.split(",")
lista_enteros = [int(n) for n in lista_de_numeros]
```

En este caso, la función “split()” toma la cadena “cadena_de_texto” y la divide en elementos separados por comas, creando una lista de cadenas. Luego, usamos una comprensión de lista para recorrer esta lista y convertir cada elemento en un número entero.

>[!TIP] TIP
> La conversión de tipos de datos es una tarea común en Python y es muy útil para realizar tareas de programación. Con las funciones de “casting” y otras herramientas, podemos convertir fácilmente valores de un tipo de datos a otro para cumplir con los requisitos de nuestro código.
