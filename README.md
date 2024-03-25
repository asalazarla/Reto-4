# Reto-4

1. Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.
```python
def es_vocal_minuscula_ascii(numero):
    """
    Evalúa si un número entero corresponde al código ASCII de alguna de las vocales minúsculas.
    
    Args:
    numero (int): El número entero a evaluar.
    
    Returns:
    bool: True si el número corresponde a una vocal minúscula, False de lo contrario.
    """
    # Definir una lista con los códigos ASCII de las vocales minúsculas.
    codigos_vocales = [97, 101, 105, 111, 117]
    
    # Comprobar si el número dado está en la lista de códigos de vocales minúsculas.
    if numero in codigos_vocales:
        return True
    else:
        return False
```

2. Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.
```python
def es_ascii_par(cadena):
    """
    Determina si el código ASCII del primer carácter de una cadena es un número par.
    
    Args:
    cadena (str): La cadena de texto cuyo primer carácter será evaluado.
    
    Returns:
    bool/None: True si el código ASCII es par, False si es impar. Retorna None si la cadena está vacía.
    """
    if cadena == "":
        # Retorna None si la cadena está vacía
        return None
    else:
        # Obtener el código ASCII del primer carácter de la cadena.
        codigo_ascii = ord(cadena[0])
        
        # Verificar si el código ASCII es par.
        if codigo_ascii % 2 == 0:
            return True
        else:
            return False
```


3. Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.
```python
def es_digito(caracter):
    """
    Verifica si el carácter proporcionado es un dígito (0-9).
    
    Args:
    caracter (str): El carácter a evaluar.
    
    Returns:
    bool: True si el carácter es un dígito, False de lo contrario.
    """
    if caracter.isdigit():
        return True
    else:
        return False
```


4. Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:

- Positivo: "El número x es positivo"
- Negativo: "El número x es negativo"
- Cero (0): "El número x es el neutro para la suma"
  
```python
def clasificar_numero(x):
    """
    Clasifica un número real como positivo, negativo o neutro (cero).
    
    Args:
    x (float): El número real a clasificar.
    
    Returns:
    str: Descripción textual de la clasificación del número.
    """
    if x > 0:
        return f"El número {x} es positivo."
    elif x < 0:
        return f"El número {x} es negativo."
    else:
        return "El número es el neutro para la suma."
```

5. Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.
   
```python
def punto_en_circulo(centro, radio, punto):
    """
    Determina si un punto está dentro de un círculo dado.
    
    Args:
    centro (tuple): Las coordenadas (x, y) del centro del círculo.
    radio (float): El radio del círculo.
    punto (tuple): Las coordenadas (x, y) del punto a evaluar.
    
    Returns:
    bool: True si el punto está dentro del círculo, False de lo contrario.
    """
    distancia = ((punto[0] - centro[0])**2 + (punto[1] - centro[1])**2)**0.5
    if distancia < radio:
        return True
    else:
        return False
```

6. Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.
```python
def es_triangulo(a, b, c):
    """
    Para que tres longitudes puedan formar un triángulo, cada par de longitudes
    sumadas debe ser mayor que la tercera longitud. Esto es conocido como la
    desigualdad triangular.
    
    Args:
    a (float): Longitud del primer lado.
    b (float): Longitud del segundo lado.
    c (float): Longitud del tercer lado.
    
    Returns:
    bool: True si las longitudes pueden formar un triángulo, False de lo contrario.
    """
    
    # Primero, comprobar que todas las longitudes sean positivas.
    if a <= 0 or b <= 0 or c <= 0:
        # Si alguna longitud no es positiva, no se puede formar un triángulo.
        return False
    # Comprobar la desigualdad triangular para cada combinación de lados.
    elif a + b > c and a + c > b and b + c > a:
        # Si todas las combinaciones cumplen la desigualdad, se puede formar un triángulo.
        return True
    else:
        # Si alguna combinación no cumple la desigualdad, no se puede formar un triángulo.
        return False        
```
