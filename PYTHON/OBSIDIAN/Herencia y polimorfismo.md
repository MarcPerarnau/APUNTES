
![](https://img.am80.com/?width=1280&url=https://assets.apuntes.de/headers/python/herencia-y-polimorfismo-en-python-amplia-la-flexibilidad-de-tus-clases.webp)

## Introducción a la herencia y el polimorfismo en Python

La **programación orientada a objetos** nos permite crear clases que pueden heredar propiedades, métodos y comportamientos de otras clases ya existentes. En Python, la herencia es una característica clave que nos permite crear clases hijas a partir de una clase padre.

La **herencia en Python** se logra por medio de una sintaxis sencilla que involucra la creación de una nueva clase que hereda atributos y métodos de la clase padre. Para crear una clase hija en Python, simplemente agregamos el nombre de la clase padre en paréntesis después del nombre de la clase hija.

**El polimorfismo**, por otro lado, es una característica que nos permite utilizar objetos de diferentes clases de manera intercambiable. Esto significa que el mismo método o función puede ser utilizado en diferentes tipos de objetos, sin preocuparnos por conocer los detalles exactos de cada uno de ellos. En Python, el polimorfismo está estrechamente relacionado con la herencia y la superposición de métodos.

La **superposición de métodos** es una técnica que nos permite modificar el comportamiento de los métodos heredados de la clase padre en la clase hija. Esto se logra al definir un método con el mismo nombre en la clase hija como en la clase padre. Cuando se llama al método en la clase hija, el intérprete de Python buscará la definición del método en la clase hija primero y, si no la encuentra, lo buscará en la clase padre.

En Python, también podemos acceder a los métodos heredados de la clase padre utilizando la función `super()`. Esto nos permite llamar al método de la clase padre directamente desde la clase hija, ahorrándonos tiempo y esfuerzo en la reescritura de código.

>  
> 
> La herencia y el polimorfismo en Python nos permiten crear clases con una mayor flexibilidad y versatilidad. Esto nos permite reutilizar código y diseñar sistemas más eficientes y escalables. Si buscas mejorar tus habilidades de programación en Python, ¡no puedes dejar de aprender sobre la herencia y el polimorfismo!

## Cómo utilizar la herencia para crear clases hijas con componentes similares pero diferentes funcionalidades

La herencia es una de las características más útiles de la programación orientada a objetos (POO) que nos permite crear clases hijas con componentes similares pero diferentes funcionalidades. En Python, esto se logra mediante la creación de una clase que hereda todas las propiedades y métodos de otra clase. Para hacer uso de esta, utilizamos la palabra clave ‘super’ para referirnos a la clase padre.

Por ejemplo, si tenemos una clase ‘Animal’ con algunas propiedades y métodos, podemos crear una clase ‘Perro’ que hereda estas propiedades y métodos. Además, podemos agregar propiedades y métodos adicionales específicos de la clase de ‘Perro’.

```python
class Animal:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def hacer_sonido(self):
        print("Este animal hace algún sonido")

class Perro(Animal):
    def __init__(self, nombre, edad, raza):
        super().__init__(nombre, edad)
        self.raza = raza

    def hacer_sonido(self):
        print("El perro hace guau guau")
```

En este ejemplo, la clase ‘Perro’ hereda las propiedades de la clase ‘Animal’ mediante la declaración de ‘(Animal)’ en su definición. Además, sobre escribe el método ‘hacer_sonido’, para que este método ahora muestre “El perro hace guau guau” en lugar de “Este animal hace algún sonido”.

Esto significa que, al **crear una instancia** de la clase ‘Perro’, podemos acceder a las propiedades y métodos de la clase ‘Animal’ y también a las nuevas propiedades y métodos de la clase ‘Perro’.

```python
mi_perro = Perro("Scottie", 3, "Terrier")
print(mi_perro.nombre) # Scottie
print(mi_perro.edad) # 3
print(mi_perro.raza) # Terrier
mi_perro.hacer_sonido() # El perro hace guau guau
```

La herencia también nos permitirá modificar o añadir nuevos métodos o atributos a la clase hija sin afectar la clase padre. En el ejemplo anterior, la clase ‘Perro’ sobrescribió el método ‘hacer_sonido’, pero también incluimos una propiedad de perro ‘raza’ que no está presente en la clase ‘Animal’.

>  
> 
> La herencia es una poderosa herramienta de programación orientada a objetos que permite a los desarrolladores crear clases hijas con componentes similares pero diferentes funcionalidades. Con Python, podemos heredar propiedades y métodos de una clase padre y anexar nuevas propiedades y métodos únicos a una clase hija.

## Cómo el polimorfismo permite a distintos objetos responder de manera diferente a un mismo llamado de método

El **polimorfismo** es una técnica de la programación orientada a objetos que permite a distintos objetos responder de manera diferente a un mismo llamado de método. En Python, esto se logra gracias al uso de **clases** y funciones, lo que aumenta significativamente la flexibilidad de nuestras implementaciones.

Una de las ventajas del polimorfismo es que nos permite escribir código más genérico, lo que a su vez nos permite reutilizar nuestro código en una variedad de situaciones. Imagina que tienes una clase **Mascota** con un método **saludar()**. Si tienes varias clases que heredan de Mascota, como **Perro** y **Gato**, cada una puede definir su propia implementación del método **saludar()**. Entonces, cuando llames a **saludar()** en un objeto de tipo Perro, la implementación de Perro se ejecutará, mientras que en un objeto de tipo Gato, la implementación de Gato se ejecutará. Esto significa que puedes escribir un método que trabaje con cualquier objeto de la clase Mascota, independientemente de si es un Perro o un Gato.

Veamos un ejemplo para entenderlo mejor. Supongamos que tenemos una clase **Figura**, que tiene un método abstracto **area()**. La idea detrás de esta clase es que cualquier figura que queramos modelar, sea un cuadrado, un círculo, un triángulo, etc., siempre tendrá una propiedad de área. Entonces, podemos crear una clase **Cuadrado** que herede de Figura y defina su propia implementación de **area()**, que calcularía el área del cuadrado. Lo mismo podemos hacer para otras figuras, como un **Círculo** o un **Triángulo**.

```py
class Figura:
    def area(self):
        pass

class Cuadrado(Figura):
    def __init__(self, lado):
        self.lado = lado

    def area(self):
        return self.lado * self.lado
```

Una vez que hemos definido nuestras clases, podemos crear un método que acepte cualquier objeto de tipo Figura, y usar el método **area()** para calcular el área de esa figura particular:

```py
def calcular_area(figura):
    return figura.area()
```

Ahora, podemos crear cualquier objeto de tipo Figura y pasarlo a nuestro método **calcular_area()**.

```py
cuadrado = Cuadrado(5)
circulo = Circulo(3)
triangulo = Triangulo(4, 5)

print(calcular_area(cuadrado))
print(calcular_area(circulo))
print(calcular_area(triangulo))
```

Esto nos dará los resultados correspondientes, calculando el área de cada una de nuestras figuras.

>  
> 
> El polimorfismo es una herramienta poderosa que nos permite reutilizar código y hacerlo más genérico. En Python, podemos implementar el polimorfismo a través del uso de clases, herencia y funciones, lo que nos da una gran flexibilidad en nuestro código. Si aún no has experimentado con el polimorfismo en Python, te animo a que lo pruebes y veas cómo puede hacer que tu código sea más flexible y fácil de leer.