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

> Fijaros que el sistema distingue mayúsculas de minúsculas, por lo que hay que tener cuidado con eso

## Números

Los números, al igual que en las matemáticas los tenemos enteros, reales, complejos… por lo que aquí tenemos un tipo para cada cosa.

Para repre