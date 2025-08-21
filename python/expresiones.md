# Python - Expresiones y funciones built-in importantes

Python incluye muchas funciones built-in que facilitan el trabajo con colecciones y datos.

# map(), filter(), zip(), enumerate(), sorted(), reversed(), any(), all()
```python!
numeros = [1,2,3,4,5]

# map(): aplica función a todos los elementos
cuadrados = list(map(lambda x: x**2, numeros))
print(cuadrados)  # [1,4,9,16,25]

# filter(): filtra elementos según condición
pares = list(filter(lambda x: x%2==0, numeros))
print(pares)  # [2,4]

# zip(): combina varias listas
letras = ["a","b","c","d","e"]
combinado = list(zip(numeros, letras))
print(combinado)  # [(1,'a'), (2,'b'), ...]

# enumerate(): obtiene índice y valor
for i, valor in enumerate(letras):
    print(i, valor)

# sorted(): devuelve lista ordenada
print(sorted([5,2,3,1]))  # [1,2,3,5]

# reversed(): invierte el iterable
print(list(reversed([1,2,3])))  # [3,2,1]

# any() y all()
print(any([0,0,1]))  # True, al menos un True
print(all([1,2,3]))  # True, todos True


## MIN, MAX, SUM, LEN, ABS
numeros = [-5, 3, 9, 0]

print(min(numeros))  # -5
print(max(numeros))  # 9
print(sum(numeros))  # 7
print(len(numeros))  # 4
print(abs(-10))      # 10

