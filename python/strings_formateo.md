# Python - Strings y formateo

Python permite manipular y formatear cadenas de manera potente y sencilla.

# Concatenación, repetición, indexing
```python!
nombre = "Styx"
saludo = "Hola " + nombre  # Concatenación
eco = nombre * 3           # Repetición
primera_letra = nombre[0]  # Indexing
ultimo = nombre[-1]         # Última letra

print(saludo, eco, primera_letra, ultimo)


## F-string
edad = 25
print(f"Hola {nombre}, tienes {edad} años")  # Hola Styx, tienes 25 años


## .format()
print("Hola {}, tienes {} años".format(nombre, edad))

# % formatting
print("Hola %s, tienes %d años" % (nombre, edad))


## Utiles de string
texto = "  Hola Mundo  "

# split y join
palabras = texto.split()         # ['Hola', 'Mundo']
unido = "-".join(palabras)      # 'Hola-Mundo'

# replace
nuevo = texto.replace("Hola", "Adiós")  # '  Adiós Mundo  '

# strip, upper, lower
limpio = texto.strip()           # 'Hola Mundo'
mayus = texto.upper()            # '  HOLA MUNDO  '
minus = texto.lower()            # '  hola mundo  '

