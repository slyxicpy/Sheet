# Listas en Python

##Creacion de listas

# Ejemplo: Acceso por índice y slicing.
# Slicing crea una nueva lista de manera optimizada sin copiar innecesariamente.
mi_lista = [10, 20, 30, 40, 50]  # Lista de ejemplo.

primer_elemento = mi_lista[0]  # Accede al primer elemento (índice 0); valor: 10.
ultimo_elemento = mi_lista[-1]  # Accede al último elemento con índice negativo; valor: 50.

sub_lista = mi_lista[1:4]  # Slicing: desde índice 1 hasta 3 (exclusivo); resultado: [20, 30, 40].
# Optimización: Usa pasos en slicing para saltar elementos.
pares = mi_lista[::2]  # Cada segundo elemento: [10, 30, 50].

# Verificación de existencia optimizada con 'in'.
# 'in' es O(n) en listas, pero para listas pequeñas es eficiente.
if 30 in mi_lista:  # Comprueba si 30 está en la lista.
    print("30 está presente")  # Esto se ejecuta

##Accesso a elementos

# Ejemplo 1: Modificación por índice.
# Eficiente porque no crea nuevas listas.
mi_lista = [1, 2, 3]  # Lista inicial.
mi_lista[1] = 20  # Cambia el elemento en índice 1 a 20; ahora: [1, 20, 3].

# Ejemplo 2: Añadir elementos con append (O(1) amortizado).
# Optimiza el crecimiento dinámico de la lista.
mi_lista.append(4)  # Añade 4 al final; ahora: [1, 20, 3, 4].

# Ejemplo 3: Extender con otra lista usando extend.
# Más eficiente que un bucle append, ya que minimiza realocaciones de memoria.
mi_lista.extend([5, 6])  # Añade múltiples elementos; ahora: [1, 20, 3, 4, 5, 6].

# Ejemplo 4: Insertar en posición específica con insert.
# O(n) en el peor caso, pero optimizado para inserciones al final.
mi_lista.insert(0, 0)  # Inserta 0 al inicio; ahora: [0, 1, 20, 3, 4, 5, 6].


##Modificado de listas!

# Ejemplo 1: Modificación por índice.
# Eficiente porque no crea nuevas listas.
mi_lista = [1, 2, 3]  # Lista inicial.
mi_lista[1] = 20  # Cambia el elemento en índice 1 a 20; ahora: [1, 20, 3].

# Ejemplo 2: Añadir elementos con append (O(1) amortizado).
# Optimiza el crecimiento dinámico de la lista.
mi_lista.append(4)  # Añade 4 al final; ahora: [1, 20, 3, 4].

# Ejemplo 3: Extender con otra lista usando extend.
# Más eficiente que un bucle append, ya que minimiza realocaciones de memoria.
mi_lista.extend([5, 6])  # Añade múltiples elementos; ahora: [1, 20, 3, 4, 5, 6].

# Ejemplo 4: Insertar en posición específica con insert.
# O(n) en el peor caso, pero optimizado para inserciones al final.
mi_lista.insert(0, 0)  # Inserta 0 al inicio; ahora: [0, 1, 20, 3, 4, 5, 6].


##Eliminado de listas!

# Ejemplo 1: Remover por valor con remove.
# Busca y elimina la primera ocurrencia (O(n)).
mi_lista = [10, 20, 30, 20]  # Lista con duplicados.
mi_lista.remove(20)  # Elimina el primer 20; ahora: [10, 30, 20].

# Ejemplo 2: Eliminar por índice con pop.
# pop() sin argumento elimina el último (O(1)); con índice es O(n).
ultimo = mi_lista.pop()  # Elimina y retorna el último; ultimo=20, lista: [10, 30].
primero = mi_lista.pop(0)  # Elimina el primero; primero=10, lista: [30].

# Ejemplo 3: Limpiar toda la lista con clear.
# Eficiente para reutilizar la lista sin crear una nueva.
mi_lista.clear()  # Ahora: [].


##Ordenado y consulta

# Ejemplo 1: Ordenar in-place con sort.
# Usa Timsort, que es O(n log n) y estable.
numeros = [5, 3, 8, 1]  # Lista desordenada.
numeros.sort()  # Ordena ascendente; ahora: [1, 3, 5, 8].
numeros.sort(reverse=True)  # Ordena descendente; ahora: [8, 5, 3, 1].

# Ejemplo 2: Ordenar con clave personalizada.
# Optimiza para ordenar objetos complejos.
palabras = ['manzana', 'banana', 'cereza']  # Lista de strings.
palabras.sort(key=len)  # Ordena por longitud; ahora: ['banana', 'cereza', 'manzana']? No: longitudes 7,6,6 -> pero sort es estable.
# Corrección: 'banana' (6), 'cereza' (6), 'manzana' (7) -> [banana, cereza, manzana].

# Ejemplo 3: Búsqueda binaria optimizada con bisect (requiere lista ordenada).
import bisect  # Importa el módulo bisect para búsquedas binarias.
lista_ordenada = [1, 3, 5, 7, 9]  # Lista ordenada.
posicion = bisect.bisect_left(lista_ordenada, 5)  # Encuentra posición para insertar/ buscar; posicion=2.
# Esto es O(log n), mucho más rápido que index() para listas grandes.


##Compresiones de listas avanzadas

# Ejemplo 1: Filtrado con condición.
# Más eficiente que bucle for + if + append.
cuadrados_pares = [x**2 for x in range(10) if x % 2 == 0]  # [0, 4, 16, 36, 64].
# Explicación: 'x**2' expresión, 'for x in range(10)' iteración, 'if x % 2 == 0' filtro.

# Ejemplo 2: Anidada para matrices.
# Optimiza la creación de listas 2D.
matriz = [[i*j for j in range(3)] for i in range(3)]  # [[0,0,0], [0,1,2], [0,2,4]].
# Explicación: Comprensión externa para filas, interna para columnas.

# Ejemplo 3: Transformación con map-like.
# Equivalente a map pero en comprensión, optimizado.
mayusculas = [s.upper() for s in ['hola', 'mundo']]  # ['HOLA', 'MUNDO'].


##Optimizaciones

# Ejemplo 1: Copia de listas con copy o slicing.
# Evita referencias compartidas.
original = [1, 2, 3]  # Lista original.
copia = original[:]  # Copia superficial con slicing; eficiente para listas planas.
# Alternativa: copia = original.copy()  # Método copy desde Python 3.3.

# Ejemplo 2: Conteo de elementos con count.
# O(n), pero optimizado internamente.
repeticiones = [1, 2, 2, 3].count(2)  # Retorna 2.

# Ejemplo 3: Reversión con reverse.
# In-place, O(n).
mi_lista = [1, 2, 3]  # Original.
mi_lista.reverse()  # Ahora: [3, 2, 1].

# Optimización general: Para listas muy grandes, considera usar arrays de numpy si solo necesitas números, ya que son más eficientes en memoria y velocidad.
# Pero para este documento, nos mantenemos en listas estándar de Python.



