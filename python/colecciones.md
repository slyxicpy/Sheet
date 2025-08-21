# Python - Operaciones con colecciones

Python ofrece métodos específicos para listas, diccionarios y sets para manipular datos fácilmente.

# Métodos de listas
```python!
lista = [1,2,3]

lista.append(4)        # [1,2,3,4]
lista.extend([5,6])    # [1,2,3,4,5,6]
lista.insert(0,0)      # [0,1,2,3,4,5,6]
lista.remove(3)        # [0,1,2,4,5,6]
lista.pop()            # 6, lista: [0,1,2,4,5]
print(lista.index(4))  # 3
print(lista.count(2))  # 1
lista.sort()           # [0,1,2,4,5]
lista.reverse()        # [5,4,2,1,0]
copia = lista.copy()   # [5,4,2,1,0]
print(copia)


## Metodos de dict
dic = {"a":1, "b":2, "c":3}

print(dic.keys())      # dict_keys(['a','b','c'])
print(dic.values())    # dict_values([1,2,3])
print(dic.items())     # dict_items([('a',1),('b',2),('c',3)])
print(dic.get("b"))    # 2
dic.update({"d":4})    # {'a':1,'b':2,'c':3,'d':4}
dic.pop("a")           # 1, dic: {'b':2,'c':3,'d':4}
dic.popitem()          # elimina último item, dic: {'b':2,'c':3}
print(dic)


## Metodos de sets
conjunto = {1,2,3}

conjunto.add(4)           # {1,2,3,4}
conjunto.remove(2)        # {1,3,4}, error si no existe
conjunto.discard(5)       # {1,3,4}, no error si no existe
otro = {3,4,5}

print(conjunto.union(otro))        # {1,3,4,5}
print(conjunto.intersection(otro)) # {3,4}
print(conjunto.difference(otro))   # {1}

