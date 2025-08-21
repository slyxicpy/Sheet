# Python - Misc

Conceptos variados importantes para escribir código limpio y correcto.

# Comentarios y docstrings
```python!
# Esto es un comentario de una línea

"""
Esto es un docstring de varias líneas
Se usa para documentar funciones, clases o módulos
"""
def ejemplo():
    """Función de ejemplo con docstring"""
    pass


## Variables globales vs locales
x = 10  # variable global

def funcion():
    global x
    x += 5  # modifica la variable global
    y = 20  # variable local
    print("Local y:", y)

funcion()
print("Global x:", x)

def externa():
    contador = 0
    def interna():
        nonlocal contador
        contador += 1
        return contador
    print(interna())  # 1
    print(interna())  # 2

externa()


## Built-in constants
print(True, False, None, Ellipsis)  # True False None Ellipsis

