# Python - Operadores

Los operadores en Python permiten realizar operaciones sobre variables y valores. Se dividen en varias categorías:

# Aritméticos
```python!
a = 10
b = 3

suma = a + b        # 13
resta = a - b       # 7
producto = a * b    # 30
division = a / b    # 3.333...
floor_div = a // b  # 3
modulo = a % b      # 1
potencia = a ** b   # 1000

## Comparacion
a = 10
b = 3

print(a == b)   # False
print(a != b)   # True
print(a > b)    # True
print(a < b)    # False
print(a >= b)   # True
print(a <= b)   # False


## Logicos
x = True
y = False

print(x and y)  # False
print(x or y)   # True
print(not x)    # False


## Asignacion
c = 5
c += 3   # c = 8
c -= 2   # c = 6
c *= 2   # c = 12
c /= 4   # c = 3.0
c %= 2   # c = 1.0
c **= 3  # c = 1.0


## Membresia
frutas = ["manzana", "banana", "cereza"]
print("banana" in frutas)      # True
print("pera" not in frutas)    # True


## Identidad
x = [1, 2, 3]
y = x
z = [1, 2, 3]

print(x is y)     # True (misma referencia)
print(x is z)     # False (mismo contenido, distinto objeto)
print(x is not z) # True

