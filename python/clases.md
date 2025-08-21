# Python - Clases y objetos

Python permite crear objetos y definir clases para organizar código y datos de manera estructurada.

# Definición de clase
```python!
class Persona:
    especie = "Humano"  # atributo de clase

    def __init__(self, nombre, edad):
        self.nombre = nombre  # atributo de instancia
        self.edad = edad

    def saludar(self):
        print(f"Hola, soy {self.nombre} y tengo {self.edad} años.")

persona1 = Persona("Styx", 25)
persona1.saludar()  # Hola, soy Styx y tengo 25 años


## Str y repr
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def __str__(self):
        return f"{self.nombre}, {self.edad} años"

    def __repr__(self):
        return f"Persona('{self.nombre}', {self.edad})"

p = Persona("Styx", 25)
print(str(p))   # Styx, 25 años
print(repr(p))  # Persona('Styx', 25)


## Herencia
class Estudiante(Persona):
    def __init__(self, nombre, edad, carrera):
        super().__init__(nombre, edad)
        self.carrera = carrera

    def estudiar(self):
        print(f"{self.nombre} está estudiando {self.carrera}")

e = Estudiante("Styx", 25, "Python Avanzado")
e.saludar()
e.estudiar()


## Encapsulacion
class Cuenta:
    def __init__(self, titular, saldo):
        self._titular = titular       # protegido
        self.__saldo = saldo          # privado

    def mostrar_saldo(self):
        print(f"Saldo: {self.__saldo}")

cuenta = Cuenta("Styx", 1000)
cuenta.mostrar_saldo()  # Saldo: 1000
# cuenta.__saldo  # Error: atributo privado


## Metodos de class
class Matematica:
    @classmethod
    def cuadrado(cls, x):
        return x**2

    @staticmethod
    def suma(a, b):
        return a + b

print(Matematica.cuadrado(5))  # 25
print(Matematica.suma(3, 7))   # 10


## Propiedades
class Rectangulo:
    def __init__(self, ancho, alto):
        self._ancho = ancho
        self._alto = alto

    @property
    def area(self):
        return self._ancho * self._alto

r = Rectangulo(5, 4)
print(r.area)  # 20

