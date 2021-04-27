---
author: Pedro Vicente Seoane Prado
layout: book
date: "2021-04-19T00:00:00.000Z"
description: Para Python, y ordenadores en general, las frases son sucesiones de caracteres, por eso los llamamamos cadenas.
---

# 🔤 Caracteres o cadenas

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
