
![](https://img.am80.com/?width=1024&url=https://assets.apuntes.de/headers/python/instalacion-de-python-en-windows-macos-y-linux-paso-a-paso.webp)
## Instalación de Python en Windows

Si estás buscando instalar Python en tu sistema operativo Windows, has llegado al lugar correcto. En este artículo, te mostraremos cómo hacerlo paso a paso.

1. **Descargar el instalador de Python**
    Lo primero que necesitas hacer es descargar el instalador de Python para Windows. Ve al sitio web oficial de Python ([https://www.python.org/downloads/windows/)](https://www.python.org/downloads/windows/%29). Asegúrate de descargar la versión más reciente de Python compatible con tu sistema operativo.
    
2. **Ejecutar el instalador**  
    Una vez que hayas descargado el archivo de instalación, haz doble clic en él para ejecutarlo. Cuando aparezca la ventana de instalación, haz clic en el botón “Install Now” para comenzar la instalación.
    
3. **Configuración de Python**
	Durante el proceso de instalación, aparecerá una ventana que te permitirá seleccionar las opciones de configuración para Python. Asegúrate de seleccionar la opción “Add Python to PATH” para que Python se pueda ejecutar desde la línea de comandos.
    
4. **Comprobar la instalación**
	Una vez finalizada la instalación, abre la línea de comandos de Windows y escribe el siguiente comando:
    ```python
    python --version
    ```
    Esto debería mostrar la versión de Python que has instalado. Si aparece un mensaje de error, es posible que debas reiniciar tu sistema para que los cambios surtan efecto.
    
5. **Instalar un entorno de desarrollo integrado (IDE)**
	Para programar en Python, necesitarás un entorno de desarrollo integrado (IDE) que te permita editar y ejecutar tu código. Hay muchas opciones de IDE disponibles, pero recomendamos utilizar Microsoft Visual Studio Code, que es una opción gratuita y muy popular en la comunidad de Python.
    Puedes descargar Visual Studio Code desde el sitio web oficial: [https://code.visualstudio.com/download](https://code.visualstudio.com/download). Una vez descargado el archivo, haz doble clic en él para ejecutarlo y sigue las instrucciones de instalación.
    
¡Listo! Ahora tienes Python instalado en tu sistema operativo Windows. Puedes empezar a escribir y ejecutar tu propio código Python usando un IDE como Visual Studio Code.

>[!TIP] TIP
> Recuerda, Python es un lenguaje de programación muy poderoso y versátil que es utilizado en muchas industrias diferentes, desde el análisis de datos hasta el desarrollo web. Si estás interesado en aprender a programar en Python, hay muchos recursos en línea gratis que puedes utilizar para empezar. ¡Buena suerte y feliz programación!
## Instalación de Python en macOS

Si eres usuario de macOS, puede que te preguntes cómo instalar Python en tu sistema operativo. No te preocupes, en esta sección te explicaremos paso a paso cómo hacerlo.

Antes de empezar, es importante que verifiques qué versión de macOS tienes instalada en tu equipo, ya que la instalación de Python puede variar dependiendo de la versión que tengas.

1. **Descarga Python**
	Entra en la página web oficial de Python y descarga la última versión de Python 3 para macOS.
    
2. **Abre el instalador**
	Una vez descargado el archivo de instalación, ábrelo y sigue los pasos que te indica el asistente de instalación.
    
3. **Selecciona los componentes que deseas instalar**
	En la ventana de selección de componentes, marca las casillas que desees instalar. Por lo general, el instalador ya selecciona los componentes necesarios por defecto.
    
4. **Configura la ubicación de instalación**
	La ubicación por defecto donde se instalará Python es en la carpeta de Aplicaciones. Si deseas cambiar la ubicación, puedes hacerlo en esta ventana.
    
5. **Introducir contraseña**
	El instalador te pedirá que introduzcas tu contraseña de usuario para poder continuar con la instalación.
    
6. **Espera hasta que se complete la instalación**
	El proceso de instalación tardará unos minutos, y una vez que finalice, aparecerá una ventana informando que la instalación ha sido completada con éxito.
    
7. **Verificación de la instalación**
	Es importante que verifiques que la instalación ha sido realizada correctamente. Para hacerlo, abre la terminal de macOS y escribe lo siguiente:
    
    ```python
    python3 --version
    ```
    
    Esto te mostrará la versión de Python que acabas de instalar.
    

## Instalación de Python en Linux

La instalación de Python en Linux es bastante sencilla, especialmente si estás familiarizado con la línea de comandos. Lo primero que debes hacer es abrir una terminal e ingresar el comando correspondiente a tu distribución de Linux.

### Instalación de Python en Ubuntu / Debian

Para instalar Python en Ubuntu o Debian, debemos ingresar los siguientes comandos:

```bash
sudo apt update
sudo apt install python3
```

Lo que estamos haciendo con el primer comando es actualizar la lista de paquetes disponibles en el repositorio. Con el segundo comando, estamos instalando Python versión 3.

Una vez completada la instalación, podemos verificar que todo esté en orden accediendo al intérprete de Python. Para ello, solo debemos escribir en la terminal `python3`. Si todo funciona bien, deberíamos obtener una pantalla que se parezca a esto:

```bash
Python 3.8.5 (default, Jan 27 2021, 15:41:15)
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

### Instalación de Python en Fedora / Red Hat

En Fedora y Red Hat, podemos instalar Python con los siguientes comandos:

```bash
sudo dnf update
sudo dnf install python3
```

Al igual que en Ubuntu y Debian, el primer comando actualiza la lista de paquetes disponibles, mientras que el segundo comando instala Python versión 3.

Para verificar que todo funciona correctamente, podemos ingresar al intérprete de Python escribiendo `python3` en la terminal. Si la instalación ha sido correcta, deberíamos ver algo así:

```bash
Python 3.9.2 (default, Feb 20 2021, 18:32:27)
[GCC 10.2.1 20210104 (Red Hat 10.2.1-9)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

### Instalación de Python en Arch Linux

En Arch Linux, podemos instalar Python con los siguientes comandos:

```bash
sudo pacman -Syu
sudo pacman -S python
```

El primer comando actualiza el sistema y la lista de paquetes disponibles, mientras que el segundo comando instala Python versión 3.

Para verificar que todo esté en orden, podemos ingresar al intérprete de Python escribiendo `python` en la terminal.

```bash
Python 3.9.2 (default, Feb 20 2021, 18:32:27)
[GCC 10.2.1 20210104 (Red Hat 10.2.1-9)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Con esto, hemos instalado Python en Linux de manera satisfactoria. Ahora solo queda disfrutar de la programación en Python en nuestra distribución Linux.