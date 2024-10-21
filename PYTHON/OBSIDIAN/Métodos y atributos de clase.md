
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/metodos-y-atributos-de-clase-en-python-funcionalidad-y-caracteristicas-compartidas.webp)

## Métodos de clase: su estructura y funcionamiento en Python

Los **métodos de clase** en Python son funciones que se definen dentro de una clase y que están diseñadas para trabajar con los atributos y objetos de dicha clase. Estos métodos tienen acceso a los atributos de la clase y pueden modificarlos, utilizarlos o devolverlos según sea necesario. En contraparte, los métodos de instancia solo tienen acceso a los atributos de la instancia.

La estructura de un método de clase es muy similar a la de una función normal en Python. Para definir un método de clase, se utiliza la palabra clave `@classmethod` antes de la definición del método. A continuación, se muestra un ejemplo sencillo:

```py
class MiClase:
    x = 1

    @classmethod
    def metodo_de_clase(cls):
        return cls.x

print(MiClase.metodo_de_clase())  # salida: 1
```

En este ejemplo, se define una clase `MiClase` con un atributo de clase `x` igual a `1` y un método de clase `metodo_de_clase` que devuelve el valor de `x` mediante la variable `cls`. Es importante notar que la variable `cls` se utiliza para referirse a la clase misma, no a una instancia de la clase.

Una de las principales **ventajas de los métodos de clase** es que se pueden utilizar para **crear múltiples constructores de una clase**. Por ejemplo, si queremos una forma diferente de crear instancias de nuestra clase `MiClase`, podemos crear un método de clase que lo permita. A continuación, se muestra un ejemplo:

```py
class MiClase:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    @classmethod
    def desde_string(cls, string):
        x, y = map(int, string.split(','))
        obj = cls(x, y)
        return obj

obj1 = MiClase(1, 2)
obj2 = MiClase.desde_string('3,4')
print(obj1.x, obj1.y)  # salida: 1 2
print(obj2.x, obj2.y)  # salida: 3 4
```

En este ejemplo, se define una clase `MiClase` con un constructor que espera dos argumentos `x` e `y`. Además, se define un método de clase `desde_string` que recibe un string con el formato `"x,y"` y crea una nueva instancia de la clase utilizando esos valores.

>  
> 
> Los métodos de clase son una herramienta muy útil en Python que permiten trabajar con los atributos y objetos de una clase de una forma más flexible y poderosa. Además, se pueden utilizar para crear diferentes constructores de una clase y simplificar la creación de instancias.

## Atributos de clase: cómo definir y utilizar variables compartidas en Python

En _Python_, las **clases** son un elemento fundamental de la programación orientada a objetos. A través de ellas, podemos definir objetos complejos que agrupan funciones y variables que comparten ciertas características. Los **atributos de clase** son precisamente variables que son compartidas por todas las instancias de una clase. A continuación, describiremos cómo se definen y utilizan estos elementos.

### Definir atributos de clase en Python

Para definir un atributo de clase, primero debemos crear la clase que lo va a contener. Por ejemplo, podemos definir una clase `MiClase` con un atributo de clase llamado `variable_compartida`:

```py
class MiClase:
    variable_compartida = 0
```

En este caso, hemos creado una clase llamada `MiClase` que no contiene ningún método ni otro atributo. Sin embargo, tiene un atributo de clase llamado `variable_compartida`, inicializado en 0. Este atributo es compartido por todas las instancias de la clase.

### Acceder a atributos de clase en Python

Para acceder a un atributo de clase desde una instancia de la misma, lo hacemos a través del nombre de la clase y el atributo en cuestión. Por ejemplo, podemos crear una instancia de `MiClase` y luego modificar su atributo de clase:

```py
instancia_1 = MiClase()
instancia_1.variable_compartida = 1
print(instancia_1.variable_compartida) # 1

instancia_2 = MiClase()
print(instancia_2.variable_compartida) # 0
```

En este ejemplo, hemos creado dos instancias de `MiClase`. La primera, `instancia_1`, tiene el atributo `variable_compartida` modificado a 1. La segunda, `instancia_2`, tiene el atributo en su valor original de 0. Esto evidencia que el atributo es compartido por todas las instancias de la clase.

También podemos acceder al atributo de clase directamente desde la propia clase, sin necesidad de instanciarla:

```py
print(MiClase.variable_compartida) # 0
```

En este caso, estamos imprimiendo el valor de `variable_compartida` directamente desde la clase `MiClase`.

### Modificar atributos de clase en Python

Para modificar el valor de un atributo de clase, basta con asignarle un nuevo valor. Al hacer esto, todas las instancias de la clase que accedan al atributo tendrán el nuevo valor:

```py
MiClase.variable_compartida = 2

print(instancia_1.variable_compartida) # 2
print(instancia_2.variable_compartida) # 2
```

En este ejemplo, hemos modificado el valor de `variable_compartida` a 2. Al acceder al atributo desde cualquiera de las instancias de `MiClase`, obtenemos el nuevo valor.

>  
> 
> Los atributos de clase permiten definir variables que son compartidas por todas las instancias de una clase. Para definirlos, basta con crear una variable dentro de la clase. Para acceder a ellos, usamos el nombre de la clase y el nombre del atributo. Para modificarlos, basta con asignarles un nuevo valor. Con estos conceptos básicos de atributos de clase en Python, podremos diseñar clases más robustas y dinámicas que nos permitan representar problemas complejos de forma sencilla.