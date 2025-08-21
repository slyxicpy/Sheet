# Python - Operadores avanzados

Python permite operaciones más complejas y elegantes con slicing, unpacking y comparaciones encadenadas.

# Slicing avanzado
```python!
lista = [0,1,2,3,4,5,6,7,8,9]
print(lista[::2])   # [0,2,4,6,8]  (cada 2 elementos)
print(lista[1::3])  # [1,4,7]      (comienza en índice 1, cada 3 elementos)
print(lista[::-1])  # [9,8,7,6,5,4,3,2,1,0] (invertir lista)


## Unpacking
# Desempaquetar lista en variables
a, b = [1, 2]
print(a, b)  # 1 2

# Unpacking con resto
lista = [1,2,3,4,5]
x, y, *rest = lista
print(x, y, rest)  # 1 2 [3,4,5]

# Unpacking en tuplas
t = (10, 20, 30)
p, *resto = t
print(p, resto)  # 10 [20,30]


## Chaining
x = 7
if 1 < x <= 10:
    print("x está entre 2 y 10")  # x está entre 2 y 10

y = 15
if 10 < y < 20:
    print("y está entre 10 y 20")  # y está entre 10 y 20

