# Tipos de datos

Aquí, vamos a simplificar mucho las cosas, vamos a explicar qué tipo de datos acepta nuestro lenguaje _\(Aunque podemos crear propios eso ya es algo más avanzado que no se dará en este curso\)_, y qué características básicas tienen.

## Números

Los números, al igual que en las matemáticas los tenemos enteros, reales, complejos… por lo que aquí tenemos un tipo para cada cosa.

| Matemático | Python | Ejemplo |
| :--- | :---: | :---: |
| Natural | `int()` | `var0 = int(128)` |
| Entero | `float()` | `var1 = float(128.256)` |
| Reales e irracionales | `float()` | `var2=float(1/3)` |
| Complejos | `complex(real,imaginaria)` | `var3=complex(3,4)` |

> Estamos suponiendo que estamos usando un sistema de 64 bits empleando el **complemento A2**, por lo que suponemos que nuestros rangos son $\[\(2^{32}\)-1,-\(2^{32}\)\]$

## Caracteres, cadenas o frases

Los ordenadores no entienden frases, pero si entienden una sucesión de caracteres delimitadas por un símbolo especial que les dice cuando detenerse, a estos niveles no es necesario saber lo que es un carácter de control.

