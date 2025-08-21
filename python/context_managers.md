# Python - Context managers

Los context managers permiten manejar recursos (archivos, conexiones, locks) garantizando que se liberen correctamente al terminar.

# with statement
```python!
# Abrir y leer un archivo usando context manager
with open("ejemplo.txt", "r") as f:
    contenido = f.read()
    print(contenido)
# No es necesario cerrar el archivo explícitamente, se cierra automáticamente


## Enter exit
class MiContexto:
    def __enter__(self):
        print("Entrando al contexto")
        return self  # opcional, se asigna si usamos 'as'

    def __exit__(self, exc_type, exc_value, traceback):
        print("Saliendo del contexto")
        if exc_type:
            print(f"Ocurrió un error: {exc_value}")
        return True  # opcional, True suprime la excepción

with MiContexto() as mc:
    print("Dentro del bloque")
    # raise ValueError("Error de prueba")  # Si se activa, no detiene el programa

