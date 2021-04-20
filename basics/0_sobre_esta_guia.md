---
author: Pedro Vicente Seoane Prado
title: Guía de estilo para Python en IPI
layout: book
date: '2021-04-19T00:00:00.000Z'
---

# Preámbulo

Esta guía está orientada al principiante en su totalidad, **no es un manual de referencia**, si no más bien una guía de estilo de cómo empezar a hacer las cosas bien, de una manera **sencilla** y **comprensible**.

En su mayoría está adaptada a la asignatura _Informática para la ingeniería_ de la _Universidade de Vigo_, en la guía docente con referencia **V01203**, por lo que estará basada en el orden de las clases.

## Preámbulo

Si bien es cierto que para qué vamos a querer crear nuestras propias herramientas teniendo cosas tan conocidas y populares como pueden ser _Matlab, Solid Works, IBM SPSS, Excel…_

Los lenguajes de programación nos permiten crear nuestra propia utilidad, a veces puede ser más útil que usar una genérica, o crear una para mejorar la funcionalidad de esos famosos programas.

En nuestro caso se ha escogido un lenguaje de alto nivel muy amigable con el usuario y fácil de aprender, vamos a trabajar con las versiones de **Python 3.x**.

> **NOTA:** para los más novatos, no busquéis información en internet demasiado dado que mucha está para versiones antiguas de Python tales como la 2 que en su mayoría no son compatibles con la 3, mejor haz caso a tus profesores.

**Con esto no vamos a decir que vayáis a ser hackers ni nada por el estilo**, tan sólo es una manera más de facilitaros la vida como ingenieros.

### Sobre el autor

Yo fui alumno de la Escuela de Ingeniería Industrial de la Universidad de Vigo, en su mención de Ingeniería Eléctrica, vi mucho más potencial a esto en mi vida que al resto de los contenidos, así que ahora ya como ingeniero informático, os voy a intentar traslar mis experiencias informáticas más bizarras a algo sencillo y que sea útil para un ingeniero mecánico, electrónico… aunque os contaré un secreto, de no ser por una gran profesora de la Universidad de Vigo, **Amparo Rodríguez Damián**, quizás ahora no estaríamos aquí, quien la tenga como profesora, tiene mucho que aprender de ella.

Actualmente trabajo con empresas tales como **Abanca Corporación Bancaria S.A.**, así que más o menos podéis fiaros de mi, pero **nunca olvidéis la curiosidad**, sin ella no hay evolución, esto es una guía de estilo, puede darte ideas, crear la tuya propia, mejora como persona [😊](https://emojiterra.com/es/sonrisa/)

## Datos básicos con los que podemos trabajar

Aquí, vamos a simplificar mucho las cosas, vamos a explicar qué tipo de datos acepta nuestro lenguaje _\(Aunque podemos crear propios eso ya es algo más avanzado que no se dará en este curso\)_, y qué características básicas tienen.

### Números

Los números, al igual que en las matemáticas los tenemos enteros, reales, complejos… por lo que aquí tenemos un tipo para cada cosa.

| Matemático | Python | Ejemplo |
| :--- | :---: | :---: |
| Natural | `int()` | `var0 = int(128)` |
| Entero | `float()` | `var1 = float(128.256)` |
| Reales e irracionales | `float()` | `var2=float(1/3)` |
| Complejos | `complex(real,imaginaria)` | `var3=complex(3,4)` |

> Estamos suponiendo que estamos usando un sistema de 64 bits empleando el **complemento A2**, por lo que suponemos que nuestros rangos son $\[\(2^{32}\)-1,-\(2^{32}\)\]$

### Caracteres, cadenas o frases

Los ordenadores no entienden frases, pero si entienden una sucesión de caracteres delimitadas por un símbolo especial que les dice cuando detenerse, a estos niveles no es necesario saber lo que es un carácter de control.

## Código abierto

A RELLENAR

## Licencia de uso

EN EL FINAL DEL LIBRO

