# RETO 4
En este reto abordamos programas bastante sencillos de programar, pero no por eso van a dejar se ser utiles para diferentes casos.

# Primer punto

Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.

```python
def esVocalAscii(num):
    vocales = ['a', 'e', 'i', 'o', 'u']
    return chr(num) in vocales

numero = int(input("Introduce un número entero: "))
print(esVocalAscii(numero))
````
- Se define una función que yo la llamé esVocalAscii que toma un número como entrada.
- Se crea una lista de vocales en minúsculas.
- Se Comprueba si el carácter correspondiente al número dado está en la lista de vocales.
- Pide al usuario que ingrese un número entero.
- Imprime True si el número ingresado es el código ASCII de una vocal minúscula, y False si no lo es.

# Segundo punto
Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.

```python
  def esAsciiPar(cadena):
    return ord(cadena[0]) % 2 == 0
  
  cadena = input("Introduce una cadena de longitud 1: ")
  print(esAsciiPar(cadena))
  ````

- Define una función llamada `esAsciiPar` que toma una cadena como entrada.
- Retorna `True` si el código ASCII del primer carácter de la cadena es par, y `False` si es impar.
- Solicita al usuario que ingrese una cadena de longitud 1.
- Imprime el resultado de llamar a la función `esAsciiPar` con la cadena ingresada. El resultado será `True` si el código ASCII del primer carácter es par, y `False` si es impar.

# Tercer punto
Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.

```python
def esDigito(caracter):
    return caracter.isdigit()

caracter = input("Introduce un carácter: ")
print(esDigito(caracter))
````
Este código en Python realiza lo siguiente:

1. Define una función llamada `esDigito` que toma un carácter como entrada.
2. Retorna `True` si el carácter es un dígito, y `False` si no lo es, utilizando el método `isdigit()`.

3. Solicita al usuario que introduzca un carácter mediante la función `input`.
4. Imprime el resultado de llamar a la función `esDigito` con el carácter ingresado. Mostrará `True` si el carácter es un dígito y `False` si no lo es.

# Cuarto punto
Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:

Positivo: "El número x es positivo"
Negativo: "El número x es negativo"
Cero (0): "El número x es el neutro para la suma"

```python
def determinarTipoNumero(x):
    if x > 0:
        return f"El número {x} es positivo"
    elif x < 0:
        return f"El número {x} es negativo"
    else:
        return f"El número {x} es el neutro para la suma"

x = float(input("Introduce un número real: "))
print(determinarTipoNumero(x))
````

1. Define una función llamada `determinarTipoNumero` que toma un número real `x`.
2. Evalúa si `x` es positivo, negativo o cero.
3. Retorna un mensaje indicando el tipo de número que es (positivo, negativo o cero).
4. Solicita al usuario que introduzca un número real.
5. Imprime el resultado de llamar a la función con el número ingresado por el usuario, indicando si es positivo, negativo o cero.

# Quinto punto
Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.

```python
def puntoEnCirculo(cx, cy, radio, px, py):
    distancia = ((px - cx) ** 2 + (py - cy) ** 2) ** 0.5
    return distancia <= radio

cx, cy = map(float, input("Introduce las coordenadas del centro (separadas por espacio): ").split())
radio = float(input("Introduce el radio del círculo: "))
px, py = map(float, input("Introduce las coordenadas del punto (separadas por espacio): ").split())

print(puntoEnCirculo(cx, cy, radio, px, py))
````

1. Define una función llamada `puntoEnCirculo` que determina si un punto dado por sus coordenadas está dentro o en la circunferencia de un círculo definido por su centro y radio.
2. Solicita al usuario que ingrese las coordenadas del centro y el radio del círculo, así como las coordenadas del punto.
3. Calcula la distancia entre el centro del círculo y el punto utilizando la fórmula de distancia euclidiana.
4. Retorna `True` si la distancia es menor o igual al radio del círculo, indicando que el punto está dentro o en la circunferencia del círculo. Retorna `False` si la distancia es mayor, indicando que el punto está fuera del círculo.
5. Imprime el resultado.

# Sexto punto
Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.

```python
def unTriangulo(a, b, c):
    return a + b > c and a + c > b and b + c > a

a, b, c = map(float, input("Introduce las tres longitudes (separadas por espacio): ").split())
print(unTriangulo(a, b, c))
````

1. Define una función llamada `unTriangulo` que determina si tres longitudes pueden formar un triángulo, aplicando la condición de la desigualdad triangular.
2. Solicita al usuario que ingrese las longitudes de los lados del triángulo.
3. Retorna `True` si las longitudes ingresadas cumplen con la desigualdad triangular (condición necesaria para formar un triángulo), y `False` si no.
4. Imprime el resultado.

Espero haya servido, ¡muchas gracias por ver!
