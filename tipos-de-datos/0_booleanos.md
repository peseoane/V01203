---
author: Pedro Vicente Seoane Prado
layout: book
date: '2021-04-19T00:00:00.000Z'
description: Los datos booleanos son aquellos que nos muestran condiciones de verdad o falsedad de manera binaria y lógica.
---

# 🙅 Dato lógico booleano

Este tipo de dato es **lógico**, quiere decir que nos puede dar dos respuestas:

* Un valor que sea `0` implica que algo es **falso**.
* Un valor que sea cualquier otro valor, usualmente `1` se considera **verdadero**.

En resumen solo admitimos que sea:

```python
>>> True    # Sólo si == 1
>>> False   # Sólo si != 1
```

> Esto no es más que la aplicación informática del álgebra booleana.
>
> Aquí el uso del operador `==` implica que algo está asignado a un valor mientras que el otro, `!=` implica que cualquier otro valor diferente al asignado. **En Python siempre se usa el orden de `operador + igual`**

El tipo de dato lógico o booleano es en computación aquel que puede representar valores de lógica binaria, esto es 2 valores, que normalmente representan falso o verdadero.1​ Se utiliza normalmente en la programación, estadística, electrónica, matemáticas (Álgebra booleana), etc.

## Tipado `bool()`

En Python el tipo de dato `bool()` es el que nos hace esta representación, podemos definirlos de varias maneras.

```python
bandera0 = True
bandera1 = False
bandera2 = bool(0)
bandera3 = bool(1)
```

Las palabras `False` y `True` están reservadas para el lenguaje, es decir, no se pueden usar como nombre de variable.

```python
 >>> True = 1 
 File "<stdin>", line 1
   True = 1
   ^
 SyntaxError: cannot assign to True

```

El error nos dice claramente que **no se puede asignar nada a `True`, forma parte de la lista de palabras reservadas.

Para comprobar que funcionan, podemos usar una **condición lógica**.

## Valores numéricos

A efectos de Python son considerados números, puedes aplicar aritmética a ellos y compararlos con números.

```python
>>> True == 1
True
>>> False == 0
True
>>> True + (False / True)
1.0
```

Llegados a este punto, los operadores booleanos sólo aceptarán entradas booleanas y por consecuencia, retornaran resultados booleanos.

### Asignar un booleano a una variable

Esto lo hemos comentado anteriormente, se puede hacer y operar con ellos sin más así.

```python
bandera0 = True
bandera1 = False
bandera2 = bool(0)
bandera3 = bool(1)
```

### Algebra booleana

Podemos trabajar con ellos con varias maneras, algunas de ellas dichas por encima son:

#### Comparadores

Aquellos que dándole dos datos, nos dirá si se cumple la condición.

##### Comparador de igualdad

Mencionado ya previamente, es aquel que nos permite saber si una variable es estrictamente igual a su asignación.

```python
>>> número = int(23)
>>> número == 23
True
>>> número == str(23)
False
>>> str(número ) == '23'
True
```

En este caso hemos creado un número entero, y le decimos si este es igual a él mismo, nos dice que sí.

Pero si lo comparamos al mismo número siendo una cadena, no es lo mismo, por lo que para ver si serían iguales podemos hacer una cosa denominada **casting** y es temporalmente convertir nuestro dato a otro para comparar si es igual a otro, comparar que el valor `int(1)` sea igual al de la cadena `str('1')`, podemos converir uno de los dos lados al otro tipo y realizar la comparación, tal que `str(variable)`.
