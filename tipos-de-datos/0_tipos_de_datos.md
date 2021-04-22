---
author: Pedro Vicente Seoane Prado
title: Tipos de datos en Python
layout: book
date: '2021-04-19T00:00:00.000Z'
description: Todo lo explicado son características inherentes y propias, no se usa ninguna herramienta o recurso externo.
---

# Tipos de datos en Python

Aquí, vamos a simplificar mucho las cosas, vamos a explicar qué tipo de datos acepta nuestro lenguaje _\(Aunque podemos crear propios eso ya es algo más avanzado que no se dará en este curso\)_, y qué características básicas tienen.

## Concepto de variable

Cuando creamos un dato o valor, se le asigna una etiqueta o identificador y se le asigna por otro lado al dato que queremos.

> A la derecha siempre va el identificador o nombre que le queremos dar a la variable, seguido de un símbolo de igualdad y el valor, es decir tal que: `nombrequeledoy = valorqueasigno`, **a esto se le conoce como declaración y asignación de una variable**.

Las variables pueden tener unos nombres determinados, hay una reglas que cumplir no todas valen, además hay palabras reservadas, pero las reglas principales son:

* Deben comenzar con un caracter.
  * Así mismo pueden contener una barra baja o dos pero son para otros usos más avanzados.
* No pueden empezar por un número
* No pueden ser una de las palabras reservadas.
  
### Palabras reservadas

Podemos comprobarlo si desde una terminal ejecutamos los siguientes comandos:

```powershell
Python 3.9.4 (tags/v3.9.4:1f2e308, Apr  4 2021, 13:27:16) [MSC v.1928 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import keyword
>>> keyword.kwlist
['False', 'None', 'True', '__peg_parser__', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
>>>
```

Las palabras anteriormente escritas no pueden ser usadas como variables.

### Ejemplo de variables admitidas

```python
nombre = str('Pedro')
Nombre = "Pedro"
NOMBRE = '''Pedro'''
Nombre1 = str("Pedro")
Nombre_1 = str('Pedro')
```

> Fijaros que el sistema distingue mayúsculas de minúsculas, por lo que hay que tener cuidado con eso.

## Números

Los números, al igual que en las matemáticas los tenemos enteros, reales, complejos… por lo que aquí tenemos un tipo para cada cosa.

Para representar cada uno de ellos, hay una asignación determinada.

### Números enteros

Aquí se engloban tanto los números enteros y naturales, y se utiliza el tipo de dato `int()`

Unos ejemplos serían:

```python
número_0 = int(0)
número_1 = int(-1)
número_2 = 3
```

> Fijaros que no es obligatorio declarar el `int()`, pero es una buena práctica para saber lo que hacemos y de paso acelerar un poco la ejecución del programa, él es lo suficientemente listo para saber que si ponemos un `1` es un entero, un `2.2` un número flotante etc...

Así mismo podemos declarar la variable vacía.

```python
número_reservado = int()
```

Pero de este modo sólo se puede dicéndole que cree un objeto de tipo `int()` ya que él por si mismo, si no le ponemos nada *a la derecha*, lógicamente no es adivino el intérprete.

**En principio no debemos preoparnos por sobrepasar un valor máximo numérico, no es necesario tener esa limitación en mente**.

### Números reales

En informática se suelen conocer más cómo números de doble precisión o flotantes, y se representan usando un punto y no una coma.

```python
pi = 3.1416
pi = float(3.1416)
```

> De nuevo ambas maneras son válidas, pero la segunda de nuevo es mejor, si tienes un programa largo en un futuro agradecerás saber qué tipo de dato querías tener ahí.

### Números complejos

Más de lo mismo, aplicamos las matemáticas que sabemos de COU/Bachillerato sin más, la designación es `complex()`.

> Cuando vemos esos paréntesis después de una palabra, eso es un **argumento**. quiere decir que se espera que dentro de esos paréntesis pongamos lo que queremos, si lo dejamos en blanco se quedará en memoria cómo un espacio reservado, pero si los ponemos deben respetar el orden, en este caso sería `complex([real[, imag]])`

Podemos hacerlo de varias maneras de nuevo:

```python
opción0 = complex(2, -3)  # Con parte imaginaria
opción1 = complex(1)      # Sin parte imaginaria
opción2 = complex()       # Espacio reservado...
opción3 = complex('5-9j') # Podemos ponerlo como una cadena ¡ENTRECOMILLARLO!
```

Y la manera menos recomendable, pues:

```python
opción0 = 2-3j
opción1 = 0j
opción2 = j     # ESTO NO FUNCIONA
opción3 = 1     # ESTO CREARÁ UN ENTERO
opción4 = complex(1) # Y ESTO UN COMPLEJO
```

**¿Ahora notáis por qué es conveniente decirle qué tipo de dato es?** al no incluír la parte imaginaria él sólo ve el número `1` y dice, pues es un entero, y si empiezas a hacer operaciones matemáticas vas a ir arrastrando errores.

### Caracteres o cadenas

En informática, de nuevo, el ordenador no entiende una frase, él lee una cadena de caracteres, que a su vez son números que representan letras, en el caso de Python 3 por defecto es la codificación UTF-8, la cuál admite todos las letras y posibles símbolos de todos los idiomas a diferencia de otras codificaciones que sólo admiten usualmente caracteres romances (alfabeto castellano, anglosajón...), pero con este sistema hasta símbolos japoneses, chinos.

**Le llamamos cadena por que es una sucesión de letras o caracteres**, y el concepto en inglés y Python es `string()`.

De nuevo podemos declarar una vacía sin asignar, darle una sóla letra o una frase.

```python
letra_vacía = string()
letra = "a"
letra = 'a'
letra = '''a'''
frase = "Hola qué tal"
frase = '''
        Hola qué tal
        '''
```

> Podéis observar que podemos delimitar usando ambos tipos de comillas siempre y cuando seamos consistentes, también la última opción mostrada suele usarse para textos más largos o documentación.

### Lógica booleana

