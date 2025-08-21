# Python - Control de flujo

El control de flujo permite dirigir la ejecución del programa según condiciones y bucles.

# Condicionales: if, elif, else
```python!
edad = 18

if edad < 13:
    print("Eres un niño")
elif edad < 20:
    print("Eres un adolescente")
else:
    print("Eres adulto")


## Bucles - for
frutas = ["manzana", "banana", "cereza"]

for fruta in frutas:
    print(fruta)

# Usando range
for i in range(5):
    print(i)  # imprime 0,1,2,3,4


## Bucles - while
contador = 0
while contador < 5:
    print(contador)
    contador += 1


## break
for i in range(10):
    if i == 5:
        break  # sale del bucle
    print(i)  # imprime 0,1,2,3,4

## continue
for i in range(5):
    if i == 2:
        continue  # salta a la siguiente iteración
    print(i)  # imprime 0,1,3,4


## Pass
for i in range(5):
    if i == 3:
        pass  # no hace nada, solo placeholder
    print(i)  # imprime 0,1,2,3,4

