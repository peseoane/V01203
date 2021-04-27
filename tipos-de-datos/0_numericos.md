---
author: Pedro Vicente Seoane Prado
layout: book
date: '2021-04-19T00:00:00.000Z'
description: Los datos más elementales, aquellos numéricos.
---

# 🔢 Números

Los números, al igual que en las matemáticas los tenemos enteros, reales, complejos… por lo que aquí tenemos un tipo para cada cosa.

Para representar cada uno de ellos, hay una asignación determinada.

## Números enteros

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

## Números reales

En informática se suelen conocer más cómo números de doble precisión o flotantes, y se representan usando un punto y no una coma.

```python
pi = 3.1416
pi = float(3.1416)
```

> De nuevo ambas maneras son válidas, pero la segunda de nuevo es mejor, si tienes un programa largo en un futuro agradecerás saber qué tipo de dato querías tener ahí.

## Números complejos

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
