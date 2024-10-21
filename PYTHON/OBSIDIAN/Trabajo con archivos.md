
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/trabajo-con-archivos-en-python-lectura-y-escritura-simplificada.webp)

## Trabajar con archivos en Python es fácil y útil

En Python, existen dos tipos principales de archivos: los **archivos de texto y los archivos binarios**. Los archivos de texto son aquellos que contienen caracteres legibles por humanos como letras y números, mientras que los archivos binarios contienen datos codificados en binario que solo las aplicaciones pueden entender. En esta ocasión, nos enfocaremos en los archivos de texto.

Para trabajar con archivos de texto en Python, lo primero que necesitamos es abrir el archivo. Esto lo podemos hacer con la función `open` de Python. Existen varias formas de usar esta función, pero la más común es especificar el nombre del archivo y el modo de apertura. Por ejemplo:

```py
archivo = open("mi_archivo.txt", "r")
```

Esta línea de código abre el archivo `mi_archivo.txt` en modo de lectura (`"r"`). Si quisieras abrir el archivo para escribir, podrías hacer lo siguiente:

```py
archivo = open("mi_archivo.txt", "w")
```

Nota que en este caso, se esta abriendo el archivo en modo de escritura (write en inglés), `'w'`.

Un tercer modo conveniente es el modo de apertura de archivos de lectura y escritura (`"r+"`):

```py
archivo = open("mi_archivo.txt", "r+")
```

Ahora que hemos abierto el archivo, podemos leer su contenido o escribir algo en él. Para leer el contenido del archivo, utilizamos la función `read`:

```py
contenido = archivo.read()
```

La variable `contenido` ahora contiene todo lo que estaba en el archivo. Si el archivo era muy grande y queremos leerlo por partes, podemos utilizar la función `readline`, que nos devuelve una línea del archivo cada vez que la llamamos:

```py
linea1 = archivo.readline()
linea2 = archivo.readline()
```

Para escribir en un archivo, utilizamos la función `write`:

```py
archivo.write("Hola, mundo!")
```

Esta línea de código escribirá la frase “Hola, mundo!” en el archivo `mi_archivo.txt`.

Una vez que hayamos terminado de trabajar con el archivo, es importante cerrarlo para liberar los recursos del sistema. Para hacerlo, utilizamos la función `close`:

```py
archivo.close()
```

>  
> 
> Trabajar con archivos en Python puede ser sencillo y útil, solo basta con conocer las funciones adecuadas. En este artículo, vimos cómo abrir, leer y escribir en archivos de texto. ¡Anímate a experimentar con tus propios archivos y verás lo poderoso que puede ser Python para manejar información!

## Cómo leer archivos en Python de forma sencilla

Leer archivos en Python puede ser un proceso complicado y tedioso debido a la gran cantidad de opciones que este lenguaje ofrece para dicha tarea. Sin embargo, existe una forma simplificada de realizarlo que puede ahorrarnos mucho tiempo y esfuerzo. En esta sección, les explicaré cómo leer archivos en Python de forma sencilla.

Lo primero que debemos hacer es abrir el archivo que vamos a leer. Para ello, podemos utilizar la función **open()** de Python, que nos permitirá especificar el nombre del archivo que vamos a leer, así como el modo de apertura en el que queremos hacerlo. En este caso, como lo que queremos es leer el archivo, utilizaremos el modo de apertura ‘r’, que indica que queremos leer el archivo en modo lectura.

```py
archivo = open('nombre_del_archivo.txt', 'r')
```

Una vez que tenemos el archivo abierto, podemos leer su contenido utilizando la función **read()**. Esta función nos permitirá leer todo el archivo completo y almacenarlo en una variable.

```py
contenido = archivo.read()
```

Una vez que hemos terminado de leer el archivo, es importante cerrarlo para liberar los recursos que se estaban utilizando. Para ello, utilizaremos la función **close()**.

```py
archivo.close()
```

¡Y listo! De esta forma tan sencilla podemos leer archivos en Python. Es importante tener en cuenta que si queremos leer un archivo que está en una ubicación diferente a la de nuestro código de Python, deberemos especificar la ruta completa del archivo.

En resumen, estos son los pasos que debemos seguir para leer archivos en Python de forma sencilla:

1. Abrir el archivo utilizando la función **open()**.
2. Leer el contenido del archivo utilizando **read()**.
3. Cerrar el archivo utilizando **close()**.

Espero que este tutorial les haya resultado de utilidad y les permita ahorrar tiempo y esfuerzo al momento de leer archivos en Python.

```py
# Ejemplo de lectura de archivo
archivo = open('prueba.txt', 'r')
contenido = archivo.read()
print(contenido)
archivo.close()
```

## Escritura de archivos con Python de manera simplificada

Una de las tareas más comunes que puede realizar cualquier programador es la escritura de archivos. Python nos proporciona una variedad de opciones para trabajar con archivos de texto y simplificar las tareas que pueden parecer difíciles a simple vista.

En nuestro caso, hemos encontrado una manera rápida y sencilla de escribir archivos con Python, utilizando el método `open()` y el modo de apertura `w` (write). Primero, abrimos el archivo en modo de escritura y a continuación, escribimos el contenido del archivo usando el método `write()`.

```py
with open('ejemplo.txt', 'w') as archivo:
    archivo.write('Hola mundo!')
```

En el código anterior, hemos creado un archivo llamado ejemplo.txt y luego hemos escrito “Hola mundo!” en su interior. Fíjate que hemos utilizado un `with` statement para que se asegure de cerrar el archivo por nosotras una vez que hayamos terminado de escribir en él.

Otro método rápido y sencillo para escribir en un archivo es utilizar la función `print()` y redirigir la salida al archivo. También podemos agregar una cadena de formato para escribir varias líneas.

```py
with open('ejemplo.txt', 'w') as archivo:
    print('Linea 1\nLinea 2\nLinea 3', file=archivo)
```

En este caso, hemos utilizado una cadena de formato que separa las líneas con caracteres de salto de línea (`\n`) y redireccionamos la salida mediante el parámetro opciona `file` de la función `print()`.

Recuerda siempre cerrar el archivo una vez que hayamos terminado de escribir en él. Python lo hace automáticamente con un `with` como en nuestro ejemplo, pero también podemos cerrar manualmente el archivo utilizando el método `close()`:

```py
archivo.close()
```

>  
> 
> La tarea de escribir archivos en Python se simplifica utilizando el método `open()` y el modo de apertura `w`. También podemos utilizar la función `print()` y redireccionar su salida al archivo. Y recuerda siempre cerrar el archivo una vez que hayas terminado de escribir en él para evitar problemas adicionales.

## Cómo utilizar la librería os para manipulación de archivos

En Python, la **librería os** permite interactuar con el sistema operativo y realizar operaciones en archivos y directorios.

Para empezar, podemos importar la librería en nuestro código:

```py
import os
```

### Verificar si un archivo existe

Para verificar si un archivo existe, podemos utilizar la función `path.exists()`, que nos devuelve `True` si existe el archivo y `False` en caso contrario.

```py
if os.path.exists('archivo.txt'):
    print('El archivo existe.')
else:
    print('El archivo no existe.')
```

### Crear un archivo

Para crear un archivo, podemos utilizar la función `open()` en modo escritura (`'w'`) y pasarle el nombre de archivo como parámetro. Luego, podemos escribir contenido en el archivo utilizando el método `write()` del objeto retornado.

```py
with open('archivo.txt', 'w') as f:
    f.write('Este es el contenido del archivo.')
```

### Leer un archivo

Para leer un archivo, podemos utilizar la función `open()` en modo lectura (`'r'`) y pasarle el nombre de archivo como parámetro. Luego, podemos leer el contenido utilizando el método `read()` del objeto retornado.

```py
with open('archivo.txt', 'r') as f:
    contenido = f.read()
    print(contenido)
```

### Renombrar un archivo

Para renombrar un archivo, podemos utilizar la función `os.rename()` y pasarle el nombre actual y el nuevo nombre del archivo como parámetros.

```py
os.rename('archivo.txt', 'archivo_renombrado.txt')
```

### Eliminar un archivo

Para eliminar un archivo, podemos utilizar la función `os.remove()` y pasarle el nombre del archivo como parámetro.

```py
os.remove('archivo_renombrado.txt')
```

### Crear un directorio

Para crear un directorio, podemos utilizar la función `os.mkdir()` y pasarle el nombre del directorio como parámetro.

```py
os.mkdir('directorio')
```

### Listar archivos y directorios

Para listar los archivos y directorios de una dirección, podemos utilizar la función `os.listdir()` y pasarle la dirección como parámetro. Esto nos devuelve una lista con los nombres de los archivos y directorios.

```py
lista = os.listdir('.')
print(lista)
```

Cabe destacar que la dirección `'.'` se refiere al directorio actual.

>  
> 
> La librería os es una herramienta muy útil para manipular archivos y directorios en Python. Con estas funciones básicas, podemos realizar muchas operaciones comunes de manipulación de archivos y directorios.

## Trucos para manejar grandes volúmenes de datos en Python

Durante mi trabajo como programador en Python, he tenido que trabajar con grandes volúmenes de datos en múltiples ocasiones. Manejar datos masivos en Python puede ser un reto, pero existen algunos trucos que pueden facilitar este proceso.

Uno de los primeros trucos a considerar es el uso de **generadores** en lugar de listas, especialmente cuando se trata de grandes conjuntos de datos. Los generadores son más eficientes en cuanto a memoria, ya que solo devuelven el valor de un elemento a la vez en lugar de almacenar la lista completa. Además, a menudo son más rápidos debido a que no tienen que cargar todos los datos en memoria antes de comenzar a procesarlos. Por ejemplo, si necesitas trabajar con cada línea de un archivo grande, puedes usar un generador que envíe cada línea una por una en lugar de leer todo el archivo en una lista.

Otro truco importante para los grandes volúmenes de datos es utilizar **bloques try-except**. Si bien esto es útil en cualquier programa, se vuelve particularmente importante al manipular grandes volúmenes de datos en los que se pueden encontrar muchos tipos diferentes de errores. En lugar de dejar que el programa se detenga en el primer error que se encuentra, puedes usar try-except para capturar el error, imprimir una descripción y continuar procesando el resto de los datos.

También es importante recordar que algunos tipos de datos pueden ser **más eficientes** que otros. Por ejemplo, los diccionarios en Python son muy rápidos para buscar y recuperar valores, lo que los hace ideales para trabajar con grandes conjuntos de datos. Si estás trabajando con datos que tienen una gran cantidad de repetición, también puedes considerar el uso de conjuntos en lugar de listas, lo que puede reducir el tiempo necesario para verificar si un elemento dado ya se encuentra en la lista.

Por último, la **paralelización** puede ser una herramienta útil para el manejo de grandes volúmenes de datos en Python. Si tienes acceso a una computadora con múltiples núcleos de CPU, puedes dividir el procesamiento en varias partes y ejecutarlas simultáneamente en diferentes núcleos. Esto puede acelerar significativamente el procesamiento de grandes volúmenes de datos.

>  
> 
> Manejar grandes volúmenes de datos en Python puede ser un reto, pero estos trucos pueden ayudarte a hacerlo de manera eficiente y efectiva. Recuerda considerar el uso de generadores, bloques try-except, tipos de datos eficientes y la paralelización para hacer que tu código sea más rápido y más efectivo en el manejo de datos masivos.