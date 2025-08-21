# Python - Archivos

Python permite leer y escribir archivos usando funciones integradas y context managers.

# Abrir, leer y escribir archivos
```python!
# Abrir y leer un archivo
archivo = open("ejemplo.txt", "r")
contenido = archivo.read()
print(contenido)
archivo.close()

# Abrir y escribir en un archivo
archivo = open("salida.txt", "w")
archivo.write("Hola, Styx!\n")
archivo.write("Segunda línea")
archivo.close()


## With
# Lectura
with open("ejemplo.txt", "r") as f:
    contenido = f.read()
    print(contenido)

# Escritura
with open("salida.txt", "w") as f:
    f.write("Esto se escribe usando with\n")


## Apertura
# r  -> leer (read)
# w  -> escribir, sobreescribe (write)
# a  -> agregar al final (append)
# rb -> leer binario
# wb -> escribir binario

# Ejemplo binario
data = bytes([10, 20, 30])
with open("archivo.bin", "wb") as f:
    f.write(data)

with open("archivo.bin", "rb") as f:
    contenido_bin = f.read()
    print(contenido_bin)  # b'\n\x14\x1e'

