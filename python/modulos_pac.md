# Python - Módulos y paquetes

Python permite organizar el código en módulos y paquetes para reutilización y claridad.

# Importar módulos
```python!
# Importar un módulo completo
import math
print(math.sqrt(16))  # 4.0

# Importar funciones específicas de un módulo
from math import pow, pi
print(pow(2,3))  # 8.0
print(pi)        # 3.141592653589793

# Importar con alias
import numpy as np
# np.array([1,2,3])  # si numpy estuviera instalado


## name=="main"
# archivo: mi_modulo.py
def saludar():
    print("Hola desde el módulo")

if __name__ == "__main__":
    # Solo se ejecuta si el archivo se corre directamente
    saludar()

# archivo: main.py
import mi_modulo
# Al importar, no se ejecuta el bloque if __name__ == "__main__"
mi_modulo.saludar()  # llama a la función explícitamente
