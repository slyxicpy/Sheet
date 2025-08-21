# Python !

## 1. Instalación

### Windows
1. Descargar desde [python.org](https://www.python.org/downloads/)
2. Ejecutar el instalador y marcar "Add Python to PATH"
3. Verificar: python --version

### Linux/mac
# Linux (Debian/Ubuntu)
sudo apt update
sudo apt install python3 python3-pip

# Mac (con Homebrew)
brew install python

  verificar : python3 --version

# Sintaxis basica!
# Comentario de una línea
"""
Docstring de varias líneas
"""

# Imprimir en pantalla
print("Hola, Styx!")

# Variables y tipos
x = 10           # entero
y = 3.14         # float
nombre = "Styx"  # string
activo = True    # boolean


## Tipos de datos basicos
int, float, str, bool
None, Elipsis


## Estructura de datos
 Listas, Tuplas, Diccionarios, Sets, Frozenset

lista = [1,2,3]
tupla = (1,2,3)
dic = {"a":1, "b":2}
conjunto = {1,2,3}


## Op
Aritméticos: +, -, *, /, //, %, **

Comparación: ==, !=, >, <, >=, <=

Lógicos: and, or, not

Asignación: =, +=, -=, etc.

Membresía: in, not in

Identidad: is, is not


## Control de flujo
x = 10
if x > 5:
    print("Mayor a 5")
else:
    print("Menor o igual 5")

for i in range(5):
    print(i)

while x > 0:
    x -= 1


## Funciones
def saludar(nombre="Styx"):
    return f"Hola {nombre}"

print(saludar())

# Lambda
suma = lambda a,b: a+b
print(suma(2,3))


## Comprension de colecciones
# List comprehension
cuadrados = [x**2 for x in range(5)]

# Dict comprehension
dic = {x:x**2 for x in range(5)}

# Set comprehension
conjunto = {x**2 for x in range(5)}


## Manejo de errores
try:
    10/0
except ZeroDivisionError:
    print("No se puede dividir entre cero")
finally:
    print("Fin del bloque")


## archivos
with open("archivo.txt","w") as f:
    f.write("Hola Styx!")

with open("archivo.txt","r") as f:
    print(f.read())


## Clases y objetos
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    def saludar(self):
        print(f"Hola, soy {self.nombre}")

p = Persona("Styx", 25)
p.saludar()


## Decoradores
def decorador(func):
    def wrapper():
        print("Antes")
        func()
        print("Después")
    return wrapper

@decorador
def hola():
    print("Hola")
hola()


## Modulos y paquetes
import math
print(math.sqrt(16))

from math import pow
print(pow(2,3))


## Funciones Built-in importantes!
numeros = [1,2,3,4]
print(list(map(lambda x:x*2, numeros)))
print(list(filter(lambda x:x%2==0, numeros)))
print(list(zip([1,2],[3,4])))
print(enumerate(["a","b"]))
print(sorted([3,1,2]))


## Strings y formateo
nombre = "Styx"
print(f"Hola {nombre}")
print("Hola {}".format(nombre))
print("Hola %s" % nombre)
texto = "  hola mundo  "
print(texto.strip().upper())


## Conversion de tipos
int("10")
float("3.14")
str(25)
bool(0)
list((1,2,3))
tuple([1,2,3])
set([1,2,3])
dict(enumerate([1,2,3]))


## OP con colecciones
# Listas
lista = [1,2]
lista.append(3)
lista.extend([4,5])
# Diccionarios
dic = {"a":1}
dic.get("a")
dic.update({"b":2})
# Sets
s = {1,2}
s.add(3)
s.union({3,4})


## OP avanzados
lista = [0,1,2,3,4,5]
print(lista[::2])
a,b,*rest = [1,2,3,4]
print(a,b,rest)
x=7
print(1<x<=10)


## Misc
# Comentarios y docstrings
# Esto es un comentario
"""
Docstring
"""
# Variables globales y locales
x=5
def f():
    global x
    x+=1


## EJEMPLO
class Persona:
    def __init__(self,nombre,edad):
        self.nombre = nombre
        self.edad = edad
    def saludar(self):
        print(f"Hola, soy {self.nombre}, tengo {self.edad} años")

p = Persona("Styx",25)
p.saludar()

