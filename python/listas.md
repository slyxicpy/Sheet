# Python - Listas|Sheet
# Las listas en Python son colecciones ordenadas y mutables que pueden contener elementos de cualquier tipo

# Crear listas
mi_lista = []
numeros = [1, 2, 3, 4, 5]
frutas = ["manzana", "banana", "cereza"]
mixta = [1, "hola", 3.14, True]

# Acceder a elementos
print(frutas[0])   # manzana
print(frutas[-1])  # cereza

# Slicing
print(numeros[1:4])   # [2, 3, 4]
print(frutas[:2])     # ['manzana', 'banana']
print(frutas[2:])     # ['cereza']
print(frutas[:])      # toda la lista

# Modificar elementos
frutas[1] = "naranja"
frutas.append("kiwi")
frutas.insert(1, "limón")
frutas.remove("manzana")
eliminado = frutas.pop()  # elimina último y lo retorna

# Operaciones útiles
len(frutas)
min(numeros)
max(numeros)
sum(numeros)

# Iterar listas
for fruta in frutas:
    print(fruta)

for i, fruta in enumerate(frutas):
    print(i, fruta)

# Ordenar y reversar
numeros.sort()
numeros.sort(reverse=True)
frutas.reverse()

# Listas por comprensión
cuadrados = [x**2 for x in range(10)]
pares = [x for x in range(10) if x % 2 == 0]

# Comprobar existencia
if "banana" in frutas:
    print("Sí hay banana")

# Copiar listas
lista_copia = frutas.copy()
lista_copia2 = frutas[:]

# Mezclar listas
otras = ["pera", "melón"]
frutas.extend(otras)
