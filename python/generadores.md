# Python - Generadores y iteradores

Los generadores e iteradores permiten recorrer secuencias de manera eficiente, especialmente con grandes conjuntos de datos.

# yield (generadores)
```python!
def generador_cuadrados(n):
    for i in range(n):
        yield i**2

for cuadrado in generador_cuadrados(5):
    print(cuadrado)
# Salida: 0, 1, 4, 9, 16


## Iter
frutas = ["manzana", "banana", "cereza"]
it = iter(frutas)  # convierte la lista en un iterador
print(it)  # <list_iterator object at 0x...>


## Next
print(next(it))  # manzana
print(next(it))  # banana
print(next(it))  # cereza
# next(it)  # StopIteration si ya no hay más elementos


## Iterables y iterators
# Iterable: objeto que se puede recorrer (list, tuple, dict, str)
lista = [1,2,3]
for x in lista:  # lista es iterable
    print(x)

# Iterator: objeto que produce los elementos uno a uno
it_lista = iter(lista)  # iterador
print(next(it_lista))  # 1
print(next(it_lista))  # 2

