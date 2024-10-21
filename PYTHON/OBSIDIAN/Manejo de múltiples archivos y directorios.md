
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/manejo-de-mltiples-archivos-y-directorios-en-python-organizacin-y-manipulacion-de-datos.webp)

## Gestionando archivos y directorios en Python

Cuando trabajamos con programas en Python, es común que necesitemos **acceder, crear, modificar o eliminar archivos y directorios en el sistema de archivos** de nuestra computadora. Por suerte, Python nos ofrece varias herramientas para llevar a cabo estas tareas de una manera sencilla.

Uno de los módulos más importantes para trabajar con archivos y directorios en Python es `os`. Este módulo nos permite interactuar con el sistema operativo en el cual estamos trabajando, y nos brinda muchas funciones útiles para manipular archivos y directorios.

Una de las primeras funciones que debemos conocer es `os.getcwd()`, que nos permite obtener el directorio de trabajo actual en el que se está ejecutando el programa. Podemos usar esta función para saber dónde se encuentran nuestros archivos o para navegar entre diferentes directorios:

```py
import os

# Obtener el directorio de trabajo actual
dir_actual = os.getcwd()

# Imprimir el directorio actual
print("Directorio actual:", dir_actual)

# Cambiar de directorio
os.chdir("..")

# Imprimir el directorio actual después del cambio
print("Nuevo directorio actual:", os.getcwd())
```

Otra función importante es `os.listdir()`, que nos permite obtener una lista con los nombres de todos los archivos y directorios que se encuentran en un directorio específico:

```py
import os

# Obtener la lista de archivos y directorios en el directorio actual
contenido_actual = os.listdir()

# Imprimir la lista de archivos y directorios
print("Contenido del directorio actual:")
for item in contenido_actual:
    print(item)
```

Para crear un nuevo archivo o directorio, podemos usar las funciones `open()` y `os.mkdir()` respectivamente. Por ejemplo, para crear un nuevo archivo de texto y escribir en él, podemos hacer lo siguiente:

```py
import os

# Crear un nuevo archivo de texto
archivo = open("nuevo_archivo.txt", "w")

# Escribir en el archivo
archivo.write("Este es un archivo de prueba")

# Cerrar el archivo
archivo.close()

# Imprimir la lista de archivos y directorios en el directorio actual
print("Contenido del directorio actual:")
for item in os.listdir():
    print(item)
```

Finalmente, para eliminar un archivo o directorio, podemos utilizar las funciones `os.remove()` y `os.rmdir()` respectivamente. Por ejemplo, para eliminar el archivo de texto que acabamos de crear, podemos hacer lo siguiente:

```py
import os

# Eliminar el archivo de texto
os.remove("nuevo_archivo.txt")

# Imprimir la lista de archivos y directorios en el directorio actual después de la eliminación
print("Contenido del directorio actual:")
for item in os.listdir():
    print(item)
```

>  
> 
> El módulo `os` nos ofrece muchas funciones útiles para gestionar archivos y directorios en Python. Con estas herramientas, podemos manipular los archivos y directorios de nuestro sistema de una manera sencilla y eficiente.

## Organizando tus archivos para una mejor manipulación

Cuando trabajamos con múltiples archivos en Python, una de las habilidades esenciales es organizar tus datos para una mejor manipulación. Manejar un gran número de archivos y directorios puede ser desalentador, pero con la planificación adecuada, puedes encontrar los archivos que necesitas de manera rápida y eficiente.

Una forma común de **organizar archivos es mediante el uso de estructuras de carpetas jerárquicas**. Por ejemplo, si estás trabajando en un proyecto de análisis de datos, puedes dividir tus datos en carpetas por mes o por año. Para hacer esto en Python, debes utilizar la herramienta `os`, que te permite crear, mover y eliminar carpetas y archivos.

```py
import os

# Crear una carpeta
os.mkdir('carpeta')

# Crear una subcarpeta dentro de la carpeta
os.mkdir('carpeta/subcarpeta')

# Acceder a una carpeta existente
os.chdir('carpeta')

# Mover un archivo a otra carpeta
os.rename('archivo.txt', 'subcarpeta/archivo.txt')

# Borrar una carpeta (y su contenido)
os.rmdir('subcarpeta')
```

Además, puedes utilizar la biblioteca `shutil` para trabajar con directorios y archivos importantes, como copiar o mover archivos. Esta biblioteca es especialmente útil cuando trabajas con archivos grandes.

```py
import shutil

# Copiar un archivo
shutil.copy('archivo_origen', 'archivo_destino')

# Mover un archivo a otra carpeta
shutil.move('archivo_origen', 'carpeta_destino')

# Borrar un archivo
os.remove('archivo.txt')
```

Para mantener una organización limpia y consistente en tus archivos y directorios, es útil nombrar tus archivos y carpetas de manera clara y lógica. Las convenciones de nomenclatura también deben ser coherentes en todo tu proyecto.

Por ejemplo, si trabajas en un proyecto que contiene conjuntos de datos basados en pdfs, podrías nombrar tus archivos usando el formato “nombre_del_archivo-fecha.pdf”. De esta manera, puedes filtrar y ordenar tus archivos rápidamente y tener una idea de cuándo se crearon.

>  
> 
> Organizar tus archivos de manera efectiva puede ahorrarte tiempo y hacer que tu trabajo sea mucho más fácil. Aprovecha las herramientas de Python para construir y mover archivos y carpetas, y desarrollo una estrategia clara para la nomenclatura de archivos y directorios. Tu proyecto y tu futuro yo te lo agradecerán.

## Como usar el modulo os en Python para navegar a través de directorios

Si alguna vez has trabajado con **múltiples archivos y directorios en Python**, sabes lo tedioso que puede ser acceder a cada archivo y hacer las tareas necesarias. Por suerte, Python tiene un modulo llamado “os” que nos facilita la vida a la hora de navegar por los diversos directorios en nuestro sistema.

El modulo os nos permite realizar tareas como crear directorios, acceder a los archivos en ellos, borrarlos, copiarlos, cambiar su nombre y mucho más. Vamos a empezar por importarlo para comenzar a trabajar.

```py
import os
```

Con esta simple línea de código, podremos empezar a utilizar las funciones que ofrece el modulo os. El primer paso para navegar por los directorios es conocer en qué directorio nos encontramos actualmente. Podemos obtener la ruta actual llamando a la función os.getcwd().

```py
ruta_actual = os.getcwd()
print(ruta_actual)
```

Esto nos dará como resultado la ruta absoluta del directorio en el que nos encontramos actualmente. Si queremos cambiar de directorio, podemos utilizar la función os.chdir().

```py
os.chdir('/ruta/nueva')
```

Este código nos llevará al directorio que indiquemos, permitiéndonos realizar las tareas necesarias en ese directorio. Para listar los archivos y directorios en la ruta actual, podemos utilizar la función os.listdir().

```py
contenido_directorio = os.listdir(ruta_actual)
print(contenido_directorio)
```

Este código nos devolverá una lista con los nombres de todos los archivos y subdirectorios en la ruta actual. Ahora que tenemos la lista de los archivos, podemos utilizar un loop para realizar las tareas necesarias en cada uno de ellos.

Por ejemplo, si queremos eliminar todos los archivos con una extensión particular, podemos hacer lo siguiente:

```py
extension = '.txt'
for archivo in contenido_directorio:
    if archivo.endswith(extension):
        os.remove(os.path.join(ruta_actual, archivo))
```

Este código eliminaría todos los archivos con la extensión “.txt” en la ruta actual. La función os.path.join() nos permite unir la ruta actual con el nombre del archivo para asegurarnos de estar eliminando el archivo correcto.

>  
> 
> El modulo os en Python es una herramienta valiosa para aquellos que trabajan con múltiples archivos y directorios en su sistema. Con las funciones que ofrece, la navegación se hace más fácil y eficiente, permitiéndonos realizar las tareas necesarias de manera más rápida y efectiva.

## Dividiendo un archivo en múltiples archivos más pequeños

Una de las cosas que más me ha costado como programador es **manejar grandes cantidades de datos en Python**. En mi trabajo diario, me encuentro con múltiples archivos de datos que deben ser procesados y manipulados. En este sentido, una de las técnicas que más me ha ayudado es la de dividir un archivo en múltiples archivos más pequeños.

Para lograr esto en Python, tenemos varias opciones. La primera es utilizar la biblioteca estándar de Python, la cual cuenta con funciones para manejar archivos y directorios. Con estas funciones, podemos leer el archivo original, dividirlo en partes y guardar cada parte en un archivo individual.

Por ejemplo, supongamos que tenemos un archivo llamado “datos.csv” con 1000 filas. Si queremos dividirlo en 10 archivos con 100 filas cada uno, podemos hacerlo de la siguiente manera:

```py
import os

with open("datos.csv") as f:
    header = next(f)  # Leer el encabezado

    for i in range(10):
        with open(f"datos_part{i+1}.csv", "w") as fw:
            fw.write(header)  # Escribir el encabezado

            for j in range(100):
                line = next(f)
                fw.write(line)
```

En este ejemplo, utilizamos un bucle `for` para crear 10 archivos llamados “datos_part1.csv” hasta “datos_part10.csv”. En cada archivo, escribimos el encabezado del archivo original y agregamos 100 filas.

Otra opción es utilizar la biblioteca pandas, que es muy útil para el análisis y procesamiento de datos. Con pandas, podemos leer el archivo original y dividirlo en partes utilizando su función `DataFrame.iloc`.

Por ejemplo, supongamos que tenemos un archivo llamado “datos.csv” con 1000 filas y 10 columnas. Si queremos dividirlo en 10 archivos con 100 filas cada uno, podemos hacerlo de la siguiente manera:

```py
import pandas as pd

df = pd.read_csv("datos.csv")
header = df.columns  # Encabezado

for i in range(10):
    df_part = df.iloc[i*100:(i+1)*100]  # Subconjunto de filas
    df_part.to_csv(f"datos_part{i+1}.csv", index=False, header=header)
```

En este ejemplo, utilizamos un bucle `for` para crear 10 archivos llamados “datos_part1.csv” hasta “datos_part10.csv”. En cada archivo, escribimos el encabezado del archivo original y agregamos 100 filas utilizando la función `DataFrame.iloc`.

>  
> 
> Dividir un archivo en múltiples archivos más pequeños es una técnica muy útil para manejar grandes cantidades de datos en Python. Podemos hacerlo utilizando la biblioteca estándar de Python o la biblioteca pandas. En ambos casos, podemos adaptar la técnica a nuestras necesidades específicas de procesamiento y manipulación de datos.

## Trabajando con archivos CSV y como manipularlos en Python

Trabajando con archivos CSV y cómo manipularlos en Python

Si estás familiarizado con la manipulación de datos, es muy probable que ya hayas trabajado con archivos CSV. Estos archivos son una forma muy común de almacenar información en tablas, como las de Excel. Si quieres aprender cómo trabajar con archivos CSV en Python, estás en el lugar correcto.

En Python, hay varias **formas de leer y escribir archivos CSV**. Para leer un archivo CSV, puedes utilizar el módulo “csv”. Por ejemplo, si tienes un archivo llamado “datos.csv” que contiene información sobre personas, puedes abrirlo e imprimir su contenido utilizando el siguiente código:

```py
import csv

with open('datos.csv', newline='') as archivo_csv:
    lector = csv.reader(archivo_csv, delimiter=',')
    for fila in lector:
        print(fila)
```

Este código abrirá el archivo “datos.csv” y lo leerá fila por fila. El parámetro “newline=’’” es necesario para asegurarte de que el lector no interprete los saltos de línea en el archivo como nuevas filas. El parámetro “delimiter=’,’” especifica que el delimitador de los datos en el archivo es una coma.

Si quieres escribir datos en un archivo CSV, también puedes utilizar el módulo “csv”. Por ejemplo, si quieres almacenar una lista de personas en un archivo llamado “nuevos_datos.csv”, puedes hacerlo utilizando el siguiente código:

```py
import csv

personas = [
    ['Juan', 'Perez', 'juanperez@email.com'],
    ['Maria', 'Gomez', 'mariagomez@email.com']
]

with open('nuevos_datos.csv', 'w', newline='') as archivo_csv:
    escritor = csv.writer(archivo_csv, delimiter=',')
    for persona in personas:
        escritor.writerow(persona)
```

Este código creará un archivo llamado “nuevos_datos.csv” y almacenará los datos de la lista “personas” en él. El parámetro “w” indica que el archivo se abrirá en modo escritura.

Además de los métodos “reader” y “writer”, el módulo “csv” también proporciona otros métodos que pueden resultar útiles, como “DictReader” y “DictWriter”. Estos métodos permiten leer y escribir archivos CSV utilizando diccionarios en lugar de listas.

>  
> 
> Trabajar con archivos CSV en Python es bastante sencillo, ya que el módulo “csv” ofrece una amplia variedad de funciones para leer y escribir este tipo de archivos. Ya sea que necesites manipular grandes cantidades de datos o simplemente estés trabajando en un proyecto pequeño, conocer cómo trabajar con archivos CSV puede ser de gran ayuda.

## Leyendo y escribiendo en archivos de texto simple en Python

Una de las tareas más comunes en el manejo de archivos con Python es la lectura y escritura de archivos de texto simple. Esto se utiliza comúnmente en aplicaciones que necesitan persistir datos o en la manipulación de archivos con información de texto, entre otros.

Para leer un archivo de texto simple en Python, podemos utilizar la función `open()` que nos permite abrir el archivo y la función `read()` que nos permite leer el contenido del mismo. Veamos un ejemplo sencillo:

```py
with open('archivo.txt', 'r') as archivo:
    contenido = archivo.read()
    print(contenido)
```

En el ejemplo anterior, abrimos un archivo llamado `archivo.txt` en modo lectura (`'r'`). Luego usamos la función `read()` para leer todo el contenido del archivo y lo almacenamos en la variable `contenido`. Finalmente, imprimimos el contenido en la consola.

Para escribir en un archivo de texto simple, podemos utilizar la función `open()` con el modo de escritura (`'w'`). Veamos un ejemplo:

```py
with open('nuevo_archivo.txt', 'w') as archivo:
    archivo.write('Este es un nuevo archivo creado desde Python.')
```

En este caso, abrimos un nuevo archivo llamado `nuevo_archivo.txt` en modo escritura (`'w'`). Luego utilizamos la función `write()` para escribir una cadena de texto en el archivo.

Es importante tener en cuenta que al utilizar la función `write()` en modo escritura (`'w'`), si el archivo ya existe, este será sobrescrito con el contenido nuevo. Si deseamos añadir contenido al final del archivo sin borrar el existente, podemos utilizar el modo de apéndice (`'a'`) en lugar del modo escritura (`'w'`).

>  
> 
> La manipulación de archivos de texto simple es una tarea bastante común en la programación con Python. Utilizando las funciones `open()` y `read()` para lectura, y `open()` y `write()` para escritura, podemos acceder a la información de los archivos y modificarla de manera sencilla.

## Cómo mover y renombrar archivos en Python

Mover y renombrar archivos en Python es una tarea común en el manejo de múltiples archivos y directorios. Afortunadamente, Python ofrece una variedad de librerías para facilitar esta tarea.

Una de las librerías más comunes para manejar archivos en Python es `os`. Esta librería contiene varias funciones para manipular archivos y directorios, incluyendo la posibilidad de mover y renombrar archivos.

Para mover un archivo a un nuevo directorio en Python, podemos utilizar la función `os.rename()` de la siguiente manera:

```py
import os

# Path original del archivo
orig_path = "/ruta/a/archivo.txt"

# Nuevo path del archivo
new_path = "/ruta/b/archivo.txt"

# Mover archivo
os.rename(orig_path, new_path)
```

En este ejemplo, estamos moviendo el archivo `archivo.txt` desde la ruta `/ruta/a/` hacia la ruta `/ruta/b/`. La función `os.rename()` toma dos argumentos: la ruta original del archivo y la nueva ruta que le queremos asignar.

Si queremos renombrar un archivo en Python, podemos utilizar la misma función `os.rename()`, pero indicando un nuevo nombre como parte de la ruta:

```py
import os

# Path original del archivo
orig_path = "/ruta/a/archivo.txt"

# Nuevo nombre del archivo
new_name = "nuevo_nombre.txt"

# Nuevo path del archivo
new_path = f"/ruta/a/{new_name}"

# Renombrar archivo
os.rename(orig_path, new_path)
```

En este ejemplo, estamos renombrando el archivo `archivo.txt` a `nuevo_nombre.txt`. Primero definimos el nombre nuevo en una variable `new_name`, y luego utilizamos este nombre para construir la nueva ruta del archivo.

Otra librería popular para manejar archivos en Python es `shutil`. Esta librería es especialmente útil cuando se trata de mover o copiar directorios completos, y contiene funciones específicas para estas tareas.

Para mover un directorio con `shutil`, podemos utilizar la función `shutil.move()` de la siguiente manera:

```py
import shutil

# Path original del directorio
orig_path = "/ruta/a/"

# Nuevo path del directorio
new_path = "/ruta/b/"

# Mover directorio
shutil.move(orig_path, new_path)
```

En este ejemplo, estamos moviendo el directorio completo ubicado en la ruta `/ruta/a/` hacia la ruta `/ruta/b/`. La función `shutil.move()` toma dos argumentos: la ruta original del directorio y la nueva ruta que le queremos asignar.

>  
> 
> Mover y renombrar archivos en Python es una tarea sencilla gracias a las librerías disponibles en el lenguaje. `os` y `shutil` son dos de las librerías más comunes para manejar archivos y directorios, y ambas ofrecen funciones específicas para mover y renombrar archivos. Con estos recursos, podemos organizar y manipular nuestros datos de manera efectiva y eficiente.

## Eliminando archivos y directorios de forma segura en Python

En el proceso de trabajo con múltiples archivos y directorios en Python, una tarea importante es eliminar los archivos o directorios que ya no son necesarios. Sin embargo, es importante asegurarse de que se eliminen de forma segura y sin perder datos importantes.

La función `os.remove()` de Python se utiliza para eliminar archivos de forma segura. Esta función elimina permanentemente el archivo que se especifica en la ruta proporcionada.

```py
import os

filename = "mi_archivo.txt"
os.remove(filename)
```

Cabe señalar que, si el archivo en cuestión está siendo utilizado por otro programa o proceso, `os.remove()` arrojará un error. Por lo tanto, es importante asegurarse de cerrar cualquier archivo antes de intentar eliminarlo.

Para eliminar directorios de forma segura, se utiliza la función `shutil.rmtree()`. Esta función elimina permanentemente el directorio especificado en la ruta proporcionada, junto con todos sus archivos y subdirectorios.

```py
import shutil

directory = "mi_directorio"
shutil.rmtree(directory)
```

Es importante tener en cuenta que eliminar un directorio y todos sus contenidos puede ser extremadamente peligroso si no se tiene cuidado. Antes de eliminar un directorio, es importante asegurarse de que no hay archivos importantes en él.

También puede ser útil utilizar la función `os.path.isdir()` para verificar si un elemento es un directorio antes de intentar eliminarlo.

```py
import os

directory = "mi_directorio"
if os.path.isdir(directory):
    shutil.rmtree(directory)
```

>  
> 
> Es importante asegurarse de que se eliminen archivos y directorios de forma segura y sin perder datos importantes. Python proporciona funciones útiles, como `os.remove()` y `shutil.rmtree()`, para eliminar archivos y directorios de forma segura. Además, es importante verificar si un elemento es un directorio antes de intentar eliminarlo.

## Cómo obtener información de los archivos en Python

Me emocioné mucho cuando empecé a trabajar con múltiples archivos y directorios en Python, pero rápidamente me di cuenta de que necesitaba saber más sobre la información de los archivos. Afortunadamente, existe una variedad de métodos disponibles para nosotros para obtener esta información.

El primer método que encontré fue la función `os.path.split()`, que nos permite dividir la ruta del archivo en dos partes: la ruta del directorio y el nombre de archivo. Esto puede ser útil cuando estamos trabajando con rutas relativas en Python:

```py
import os

ruta_archivo = 'archivos/misdatos.txt'
ruta_directorio, nombre_archivo = os.path.split(ruta_archivo)

print(ruta_directorio)
# salida: 'archivos/'

print(nombre_archivo)
# salida: 'misdatos.txt'
```

También podemos utilizar la función `os.path.splitext()`, la cual nos permite separar el nombre de archivo y la extensión:

```py
ruta_archivo = 'archivos/misdatos.txt'
nombre_archivo, extension = os.path.splitext(ruta_archivo)

print(nombre_archivo)
# salida: 'misdatos'

print(extension)
# salida: '.txt'
```

Por otro lado, la función `os.path.isdir()` nos permitirá determinar si la ruta que estamos explorando corresponde a un directorio o no:

```py
ruta = 'archivos/'

if os.path.isdir(ruta):
    print(f'{ruta} es un directorio')
else:
    print(f'{ruta} NO es un directorio')
```

La función `os.path.isfile()` nos ayuda a determinar si la ruta corresponde a un archivo o no:

```py
ruta = 'archivos/misdatos.txt'

if os.path.isfile(ruta):
    print(f'{ruta} es un archivo')
else:
    print(f'{ruta} NO es un archivo')
```

Además, si necesitamos obtener detalles adicionales sobre un archivo, podemos utilizar la función `os.stat()`. Esta función nos devolverá un objeto que contiene información como la fecha de creación, la fecha de última modificación, y el tamaño del archivo, entre otras cosas. Podemos acceder a estas propiedades mediante el uso de los métodos del objeto que nos devuelve `os.stat()`:

```py
ruta = 'archivos/misdatos.txt'
datos_archivo = os.stat(ruta)

print(f'Fecha de creación: {datos_archivo.st_ctime}')
print(f'Fecha de última modificación: {datos_archivo.st_mtime}')
print(f'Tamaño del archivo: {datos_archivo.st_size}')
```

Con estos métodos, podemos obtener información valiosa de nuestros archivos y directorios en Python, lo cual nos permitirá manipular y organizar nuestros datos con mayor eficiencia y precisión.

## Ejemplos prácticos de manipulación de archivos y directorios en Python

Después de aprender acerca de cómo manejar múltiples archivos y directorios en Python, estamos listos para aplicar nuestros conocimientos en ejemplos prácticos. Aquí presentamos algunos ejemplos sencillos que muestran cómo podemos manipular archivos y directorios con Python.

### Ejemplo 1: Crear un nuevo directorio

Supongamos que queremos crear un nuevo directorio llamado ‘datos’ en nuestra carpeta de trabajo actual. Podemos hacerlo usando la función `mkdir` del módulo `os`.

```py
import os

os.mkdir('datos')
```

Con esto hemos creado un nuevo directorio llamado ‘datos’.

### Ejemplo 2: Mover un archivo a un nuevo directorio

Supongamos que tenemos un archivo llamado ‘ventas.csv’ en nuestra carpeta de trabajo y queremos moverlo al directorio ‘datos’ que acabamos de crear. Podemos hacerlo usando la función `rename` del módulo `os`.

```py
import os

os.rename('ventas.csv', 'datos/ventas.csv')
```

Con esto hemos movido el archivo ‘ventas.csv’ al directorio ‘datos’.

### Ejemplo 3: Listar los archivos de un directorio

Supongamos que queremos listar todos los archivos que están en el directorio actual. Podemos hacer uso de la función `listdir` del módulo `os`.

```py
import os

archivos = os.listdir('.')
for archivo in archivos:
    print(archivo)
```

Con esto hemos impreso una lista de todos los archivos que se encuentran en la carpeta actual.

### Ejemplo 4: Eliminar un archivo

Supongamos que queremos eliminar el archivo ‘ventas.csv’. Podemos hacer esto usando la función `remove` del módulo `os`.

```py
import os

os.remove('ventas.csv')
```

Con esto hemos eliminado el archivo ‘ventas.csv’.

>  
> 
> Como podemos ver, Python ofrece una gran variedad de herramientas para trabajar con archivos y directorios. Con estos ejemplos, esperamos haber podido ilustrar algunos de los usos más comunes de estas herramientas. ¡Te animamos a seguir aprendiendo y experimentando con todo lo que Python tiene para ofrecer!