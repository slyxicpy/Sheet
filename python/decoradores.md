# Python - Decoradores

Los decoradores permiten modificar o extender el comportamiento de funciones sin cambiar su código interno.

# Funciones decoradoras simples
```python!
def decorador(func):
    def envoltura():
        print("Antes de la función")
        func()
        print("Después de la función")
    return envoltura

@decorador
def saludar():
    print("Hola, Styx!")

saludar()
# Salida:
# Antes de la función
# Hola, Styx!
# Después de la función


## Parametros
def repetir_veces(n):
    def decorador(func):
        def envoltura(*args, **kwargs):
            for _ in range(n):
                func(*args, **kwargs)
        return envoltura
    return decorador

@repetir_veces(3)
def decir_hola():
    print("Hola!")

decir_hola()
# Salida:
# Hola!
# Hola!
# Hola!

