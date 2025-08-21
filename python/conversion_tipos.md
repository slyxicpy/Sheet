# Python - Conversión de tipos

Python permite convertir entre distintos tipos de datos usando funciones built-in.

# Conversión de tipos
```python!
# Números
a = "10"
b = int(a)       # 10 (str -> int)
c = float(a)     # 10.0 (str -> float)

# Booleanos
print(bool(0))   # False
print(bool(1))   # True
print(bool(""))  # False
print(bool("hola"))  # True

# Strings
num = 25
texto = str(num)  # '25'

# Colecciones
lista = [1,2,3]
tupla = tuple(lista)  # (1,2,3)
conjunto = set(lista) # {1,2,3}
diccionario = dict(enumerate(lista))  # {0:1, 1:2, 2:3}

print(b, c, texto, tupla, conjunto, diccionario)

