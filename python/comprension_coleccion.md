# Python - Comprensión de colecciones

La comprensión de colecciones permite crear listas, diccionarios o conjuntos de manera concisa y legible.

# List comprehension
```python!
# Crear lista de cuadrados
cuadrados = [x**2 for x in range(6)]
print(cuadrados)  # [0, 1, 4, 9, 16, 25]

# Filtrar elementos
pares = [x for x in range(10) if x % 2 == 0]
print(pares)  # [0, 2, 4, 6, 8]

## Dict comprehension
# Crear diccionario con números y sus cuadrados
cuadrados_dict = {x: x**2 for x in range(6)}
print(cuadrados_dict)  # {0:0, 1:1, 2:4, 3:9, 4:16, 5:25}

# Filtrar elementos
pares_dict = {x: x**2 for x in range(10) if x % 2 == 0}
print(pares_dict)  # {0:0, 2:4, 4:16, 6:36, 8:64}


## Set comprehension
# Crear conjunto con cuadrados
cuadrados_set = {x**2 for x in range(6)}
print(cuadrados_set)  # {0, 1, 4, 9, 16, 25}

# Filtrar elementos
pares_set = {x for x in range(10) if x % 2 == 0}
print(pares_set)  # {0, 2, 4, 6, 8}

