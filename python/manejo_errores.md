# Python - Manejo de errores

Python permite capturar y manejar errores para que el programa no se detenga inesperadamente.

# try, except, else, finally
```python!
try:
    x = int(input("Ingresa un número: "))
    resultado = 10 / x
except ValueError:
    print("¡Eso no es un número válido!")
except ZeroDivisionError:
    print("No se puede dividir entre cero.")
else:
    print(f"El resultado es {resultado}")
finally:
    print("Fin del bloque de manejo de errores")


## Built-in
# ValueError
int("hola")  # lanza ValueError

# TypeError
suma = "hola" + 5  # lanza TypeError

# IndexError
lista = [1,2,3]
lista[5]  # lanza IndexError


## Raise
def dividir(a, b):
    if b == 0:
        raise ValueError("b no puede ser cero")
    return a / b

try:
    dividir(10,0)
except ValueError as e:
    print(f"Error capturado: {e}")

