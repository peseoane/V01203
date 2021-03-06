---
author: Pedro Vicente Seoane Prado
layout: book
date: "2021-04-19T00:00:00.000Z"
description: Los datos booleanos son aquellos que nos muestran condiciones de verdad o falsedad de manera binaria y l贸gica.
---

# 馃檯 Dato l贸gico booleano

Este tipo de dato es **l贸gico**, quiere decir que nos puede dar dos respuestas:

- Un valor que sea `0` implica que algo es **falso**.
- Un valor que sea cualquier otro valor, usualmente `1` se considera **verdadero**.

En resumen solo admitimos que sea:

```python
>>> True    # S贸lo si == 1
>>> False   # S贸lo si != 1
```

> Esto no es m谩s que la aplicaci贸n inform谩tica del 谩lgebra booleana.
>
> Aqu铆 el uso del operador `==` implica que algo est谩 asignado a un valor mientras que el otro, `!=` implica que cualquier otro valor diferente al asignado. **En Python siempre se usa el orden de `operador + igual`**

El tipo de dato l贸gico o booleano es en computaci贸n aquel que puede representar valores de l贸gica binaria, esto es 2 valores, que normalmente representan falso o verdadero.1鈥? Se utiliza normalmente en la programaci贸n, estad铆stica, electr贸nica, matem谩ticas (脕lgebra booleana), etc.

## Tipado `bool()`

En Python el tipo de dato `bool()` es el que nos hace esta representaci贸n, podemos definirlos de varias maneras.

```python
bandera0 = True
bandera1 = False
bandera2 = bool(0)
bandera3 = bool(1)
```

Las palabras `False` y `True` est谩n reservadas para el lenguaje, es decir, no se pueden usar como nombre de variable.

```python
 >>> True = 1
 File "<stdin>", line 1
   True = 1
   ^
 SyntaxError: cannot assign to True

```

El error nos dice claramente que \*\*no se puede asignar nada a `True`, forma parte de la lista de palabras reservadas.

Para comprobar que funcionan, podemos usar una **condici贸n l贸gica**.

## Valores num茅ricos

A efectos de Python son considerados n煤meros, puedes aplicar aritm茅tica a ellos y compararlos con n煤meros.

```python
>>> True == 1
True
>>> False == 0
True
>>> True + (False / True)
1.0
```

Llegados a este punto, los operadores booleanos s贸lo aceptar谩n entradas booleanas y por consecuencia, retornaran resultados booleanos.

### Asignar un booleano a una variable

Esto lo hemos comentado anteriormente, se puede hacer y operar con ellos sin m谩s as铆.

```python
bandera0 = True
bandera1 = False
bandera2 = bool(0)
bandera3 = bool(1)
```

### Algebra booleana

Podemos trabajar con ellos con varias maneras, algunas de ellas dichas por encima son sin emplear operadores al uso.

Podemos usar l贸gica t铆pica tal que `and`, `not`, `or`... conceptos de grupos y conjuntos.

```python
>>> if True:
...     print(True)
True
>>> not True
False
>>> True and True
True
>>> True and False
False
>>> True or False
True
>>> not False
True
```

Y as铆 eternamente.

#### Comparadores

Aquellos que d谩ndole dos datos, nos dir谩 si se cumple la condici贸n.

##### Comparador de igualdad

Mencionado ya previamente, es aquel que nos permite saber si una variable es estrictamente igual a su asignaci贸n.

```python
>>> n煤mero = int(23)
>>> n煤mero == 23
True
>>> n煤mero == str(23)
False
>>> str(n煤mero ) == '23'
True
```

En este caso hemos creado un n煤mero entero, y le decimos si este es igual a 茅l mismo, nos dice que s铆.

Pero si lo comparamos al mismo n煤mero siendo una cadena, no es lo mismo, por lo que para ver si ser铆an iguales podemos hacer una cosa denominada **casting** y es temporalmente convertir nuestro dato a otro para comparar si es igual a otro, comparar que el valor `int(1)` sea igual al de la cadena `str('1')`, podemos converir uno de los dos lados al otro tipo y realizar la comparaci贸n, tal que `str(variable)`.

##### Comparadores de orden (conjuntos)

Los clasificaciamos principalmente en aquellos que pueden darnos:

- Rangos abiertos: aquellos que queremos saber si algo es mayor o menos que algo.
- Rangos cerrados: aquellos en lo que queremos saber si algo es mayor o igual a algo, y viceversa, menor o igual a un valor dado.

```python
# Comparadores escritos
>>> numero0 = int(10)
>>> numero1 = int(11)
...
>>> numero0 > numero1
False
>>> numero0 < numero1
True
>>> numero0 >= numero1
False
>>> numero0 <= numero1
True
```

##### Comparadores de inclusi贸n

Aqu铆 comparamos si algo es exactamente otro valor, pero a diferencia del comparador `==` y `!=` estos adem谩s comparan el tipo de objeto, es decir debe ser el mismo valor, tipo de dato y todo exactamente igual, no valen con que sus datos coincidan.

Un ejemplo...

```python
>>> numero0 = int(0)
>>> numero1 = float(0)
>>> numero0 == numero1
True
>>> numero0 is numero1
False
```

En el primer caso nos dice que si, los dos ceros son iguales, pero en el segundo nos dice que claro, no es la misma identidad, no es lo mismo un n煤mero entero `int()` que un real `float()`.

De ah铆 la importancia de declarar el tipo de dato previamente, si no...

```python
>>> numero0 = 0
>>> numero1 = 0
>>> numero0 == numero1
True
>>> numero0 is numero1
True
```

Usando la funci贸n integrada `type(var)` nos dir谩 qu茅 ha pasado:

```python
# PRIMER CASO
>>> numero0 = int(0)
>>> numero1 = float(0)
>>> type(numero0)
<class 'int'>
>>> type(numero1)
<class 'float'>

# SEGUNDO CASO
>>> type(numero0)
<class 'int'>
>>> type(numero1)
<class 'int'>

# ALTERVATIVA
>>> numero1 = 0.0
>>> type(numero1)
<class 'float'>
```

**La lecci贸n aqu铆** es qu茅 es importante declarar bien los datos o luego las comparaciones podr谩n hacernos extra帽os, como alternativa, hab茅is visto que poner un `0.0` lo asigna a flotante, pero de otro modo 茅l siempre se pone en el modo m谩s sencillo.

El an谩logo de `is` ser铆a `not`.

En este caso se hace la uni贸n de \*el dato de la derecha no es exactamente el mismo que el segundo\*\*.

Poner un `not` solitario no funcionar谩. 馃槬

```python
# BIEN HECHO
>>> numero0 is not numero1
True
# MAL HECHO
>>> numero0 not numero1
  File "<stdin>", line 1
    numero0 not numero1
                ^
SyntaxError: invalid syntax
```

##### Comparadores de presencia

WIP
