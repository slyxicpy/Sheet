# Python - Funciones

Las funciones en Python permiten agrupar código reutilizable y parametrizable.

# Definición con def
```python!
def saludar(nombre):
    print(f"Hola, {nombre}!")

saludar("Styx")  # Hola, Styx!


# Argumentos
# Posicionales y keyword
def info_persona(nombre, edad=0):
    print(f"Nombre: {nombre}, Edad: {edad}")

info_persona("Styx")         # Nombre: Styx, Edad: 0
info_persona("Styx", edad=25) # Nombre: Styx, Edad: 25

# *args: número variable de argumentos
def suma_todos(*args):
    return sum(args)

print(suma_todos(1,2,3,4))  # 10

# **kwargs: argumentos con nombre variable
def mostrar_info(**kwargs):
    for k, v in kwargs.items():
        print(f"{k}: {v}")

mostrar_info(nombre="Styx", ciudad="Quito")


## retorno - return
def cuadrado(x):
    return x**2

resultado = cuadrado(5)  # 25


## Lambda
doblar = lambda x: x*2
print(doblar(4))  # 8


## Funciones anidada
def multiplicador(factor):
    def multiplicar(n):
        return n * factor
    return multiplicar

doble = multiplicador(2)
print(doble(5))  # 10


## Funciones recursivas
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

print(factorial(5))  # 120

