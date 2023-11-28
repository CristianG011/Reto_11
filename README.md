# Reto_11

# Desarrolle un programa que permita realizar la suma/resta de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.
```python
import random

def crear_matriz_1(filas1, columnas1):
    matriz_1 = []
    for x in range(filas1):
        fila1 = []
        for y in range(columnas1):
            fila1.append(random.randint(1, 100))
        matriz_1.append(fila1)
    return matriz_1

def crear_matriz_2(filas2, columnas2):
    matriz_2 = []
    for m in range(filas2):
        fila2 = []
        for n in range(columnas2):
            fila2.append(random.randint(1, 100))
        matriz_2.append(fila2)
    return matriz_2

if __name__ == "__main__":
    filas1 = int(input("Ingrese el número de filas para la matriz 1: "))
    columnas1 = int(input("Ingrese el número de columnas para la matriz 1: "))
    filas2 = int(input("Ingrese el número de filas para la matriz 2: "))
    columnas2 = int(input("Ingrese el número de columnas para la matriz 2: "))
    matriz_1 = crear_matriz_1(filas1, columnas1)
    matriz_2 = crear_matriz_2(filas2, columnas2)


print("Su primera matriz es: ")
print(matriz_1)
print("Su segunda matriz es: ")
print(matriz_2)
def sumar_matrices(matriz_1, matriz_2):
  if len(matriz_1) != len(matriz_2) or len(matriz_1[0]) != len(matriz_2[0]):
    print("No se pueden sumar matrices de tamaños diferentes.")
    return None

  resultado = []
  for i in range(len(matriz_1)):
      fila_resultado = []
      for j in range(len(matriz_1[0])):
          suma_elemento = matriz_1[i][j] + matriz_2[i][j]
          fila_resultado.append(suma_elemento)
      resultado.append(fila_resultado)

  return resultado

def resta_matrices(matriz1, matriz_2):
  if len(matriz_1) != len(matriz_2) or len(matriz_1[0]) != len(matriz_2[0]):
    print("No se pueden sumar matrices de tamaños diferentes.")
    return None

  resultado = []
  for i in range(len(matriz_1)):
      fila_resultado = []
      for j in range(len(matriz_1[0])):
          suma_elemento = matriz_1[i][j] - matriz_2[i][j]
          fila_resultado.append(suma_elemento)
      resultado.append(fila_resultado)

  return resultado
suma = sumar_matrices(matriz_1, matriz_2)
if suma is not None:
  print("Su suma es: ")
  print(suma)

resta = resta_matrices(matriz_1, matriz_2)
if suma is not None:
  print("Su resta es: ")
  print(resta)
```
# Desarrolle un programa que permita realizar el producto de matrices. El programa debe validar las condiciones necesarias para ejecutar la operación.
import random
```python
def crear_matriz_1(filas1, columnas1):
    matriz_1 = []
    for x in range(filas1):
        fila1 = []
        for y in range(columnas1):
            fila1.append(random.randint(1, 100))
        matriz_1.append(fila1)
    return matriz_1

def crear_matriz_2(filas2, columnas2):
    matriz_2 = []
    for m in range(filas2):
        fila2 = []
        for n in range(columnas2):
            fila2.append(random.randint(1, 100))
        matriz_2.append(fila2)
    return matriz_2

if __name__ == "__main__":
    filas1 = int(input("Ingrese el número de filas para la matriz 1: "))
    columnas1 = int(input("Ingrese el número de columnas para la matriz 1: "))
    filas2 = int(input("Ingrese el número de filas para la matriz 2: "))
    columnas2 = int(input("Ingrese el número de columnas para la matriz 2: "))
    matriz_1 = crear_matriz_1(filas1, columnas1)
    matriz_2 = crear_matriz_2(filas2, columnas2)


print("Su primera matriz es: ")
print(matriz_1)
print("Su segunda matriz es: ")
print(matriz_2)


def producto_matriz(matriz_1, matriz_2):
  if len(matriz_1[0]) != len(matriz_2):
    print("No se puede calcular el producto de matrices con estas dimensiones, recuerda que la primera debe tener el mismo número de columnas que filas la segunda")
    return None
  resultado = []
  for i in range(len(matriz_1)):
    fila_resultado = []
    for j in range(len(matriz_2[0])):
      suma = 0
      for k in range(len(matriz_2)):
        suma += matriz_1[i][k] * matriz_2[k][j]
      fila_resultado.append(suma)
    resultado.append(fila_resultado)

  return resultado
producto = producto_matriz(matriz_1, matriz_2)
if producto is not None:
  print("Resultado del producto de matrices:")
  print(producto)
```
# Desarrolle un programa que permita obtener la matriz transpuesta de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la operación.
```python
import random

def crear_matriz_1(filas1, columnas1):
    matriz_1 = []
    for x in range(filas1):
        fila1 = []
        for y in range(columnas1):
            fila1.append(random.randint(1, 100))
        matriz_1.append(fila1)
    return matriz_1

if __name__ == "__main__":
    filas1 = int(input("Ingrese el número de filas para la matriz 1: "))
    columnas1 = int(input("Ingrese el número de columnas para la matriz 1: "))
    matriz_1 = crear_matriz_1(filas1, columnas1)
print("Su primera matriz es: ")
print(matriz_1)

def matriz_transpuesta(matriz_1):
    filas = len(matriz_1)
    columnas = len(matriz_1[0])
    transpuesta = [[0] * filas for _ in range(columnas)]
    for i in range(filas):
        for j in range(columnas):
            transpuesta[j][i] = matriz_1[i][j]

    return transpuesta

transpuestaa = matriz_transpuesta(matriz_1)
print("La matriz transpuesta es:")
print(transpuestaa)
```
# Desarrollar un programa que sume los elementos de una columna dada de una matriz.
```python
import random

def crear_matriz_1(filas1, columnas1):
    matriz_1 = []
    for x in range(filas1):
        fila1 = []
        for y in range(columnas1):
            fila1.append(random.randint(1, 100))
        matriz_1.append(fila1)
    return matriz_1

def sumar_culumna(matriz_1, columna_dada):
    if columna_dada < 0 or columna_dada >= len(matriz_1[0]):
        print("Número de columna no válido.")
        return None

    suma = 0
    for fila in matriz_1:
        suma += fila[columna_dada]

    return suma
if __name__ == "__main__":
    filas1 = int(input("Ingrese el número de filas para la matriz 1: "))
    columnas1 = int(input("Ingrese el número de columnas para la matriz 1: "))
    columna_dada = int(input("Ingrese la columna elegida "))
    matriz_1 = crear_matriz_1(filas1, columnas1)
    resultado_suma = sumar_culumna(matriz_1, columna_dada)

print("Su matriz es: ")
print(matriz_1)
print("La suma de su colunma es: ")
print(resultado_suma)
```
# Desarrollar un programa que sume los elementos de una fila dada de una matriz.
```python
import random

def crear_matriz_1(filas1, columnas1):
    matriz_1 = []
    for x in range(filas1):
        fila1 = []
        for y in range(columnas1):
            fila1.append(random.randint(1, 100))
        matriz_1.append(fila1)
    return matriz_1
def sumar_filas(matriz_1, fila_dada):
  if fila_dada < 0 or fila_dada >= len(matriz_1):
   print("Número de fila no válido.")
   return None
  suma = 0
  for elemento in matriz_1[fila_dada]:
        suma += elemento

  return suma
if __name__ == "__main__":
    filas1 = int(input("Ingrese el número de filas para la matriz 1: "))
    columnas1 = int(input("Ingrese el número de columnas para la matriz 1: "))
    fila_dada = int(input("Ingrese la fila elegida "))
    matriz_1 = crear_matriz_1(filas1, columnas1)
    resultado_suma = sumar_filas(matriz_1, fila_dada)

print("Su matriz es: ")
print(matriz_1)
print("La suma de fila es: ")
print(resultado_suma)



