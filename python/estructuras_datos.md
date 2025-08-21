# Python - Estructuras de datos

Las estructuras de datos en Python permiten almacenar y organizar colecciones de elementos de manera eficiente.

# Listas! (list)
```python
# Crear listas
numeros = [1, 2, 3, 4, 5]
frutas = ["manzana", "banana", "cereza"]
mixta = [1, "hola", 3.14, True]

# Acceder a elementos
print(frutas[0])   # manzana
print(frutas[-1])  # última posición

# Modificar elementos
frutas[1] = "naranja"
frutas.append("kiwi")
frutas.insert(1, "limón")
frutas.remove("manzana")
eliminado = frutas.pop()

# Operaciones
len(frutas)
frutas.count("kiwi")
frutas.index("kiwi")
frutas.sort()
frutas.reverse()

## Tuplas
# Crear tuplas
coordenadas = (10, 20)
colores = ("rojo", "verde", "azul")

# Acceder a elementos
print(colores[0])
print(coordenadas[1])

# Las tuplas son inmutables, no se pueden modificar

## Dict - Diccionario
# Crear diccionarios
persona = {"nombre": "Styx", "edad": 25, "pais": "Ecuador"}

# Acceder a elementos
print(persona["nombre"])
print(persona.get("edad"))

# Modificar o agregar elementos
persona["edad"] = 26
persona["profesion"] = "Programador"

# Métodos útiles
persona.keys()
persona.values()
persona.items()
persona.pop("pais")
persona.update({"pais": "España"})


## Sets - conjuntos
# Crear conjuntos
frutas_set = {"manzana", "banana", "cereza"}

# Operaciones
frutas_set.add("kiwi")
frutas_set.remove("banana")
frutas_set.union({"pera", "melón"})
frutas_set.intersection({"cereza", "kiwi"})
frutas_set.difference({"manzana"})


## Frozenset
# Conjunto inmutable
conjunto_inmutable = frozenset([1, 2, 3, 4])

# No se pueden añadir ni eliminar elementos
# operaciones como union, intersection, difference devuelven un nuevo frozenset
nuevo = conjunto_inmutable.union([4, 5, 6])

