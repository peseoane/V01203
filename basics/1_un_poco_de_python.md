# Python

Debo de suponer que no sabes absolutamente nada de programación, por lo que intentaré explicarte de manera muy amigable todo lo que pueda.

Vamos a suponer el primer problema que uno debe afrontar al aprender un lenguaje, y es hacer un `hola mundo`, el código sería algo así:

```python
if __name__ == '__main__':
    print('Hola mundo')
```

Y lo que veríamos por pantalla sería esto otro una vez ejecutado:

```bash
 /m/c/U/seoan  python3
Python 3.8.5 (default, Jan 27 2021, 15:41:15)
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> if __name__ == '__main__':
...     print('Hola mundo')
...
Hola mundo
>>>
```

## ¿No hay un archivo fuente que compilar?

No, en el caso anterior, tan sólo he abierto el programa desde la terminal, he escrito la función y me ha devuelto la respuesta, a esto se le conoce como ==modo intérprete==. Funciona como una súper-calculadora básicamente, la enciendes y le das a las teclas. [😉](https://emojiterra.com/es/guinando-el-ojo/)

## ¿Y si prefiero un enfoque más tradicional?

Lógicamente, guardaríamos ese texto en un fichero `holamundo.py` y lo ejecutaríamos desde la terminal.

```bash
 ⚙  /tmp  nano holamundo.py
 ⚙  /tmp  python3 holamundo.py
Hola mundo
```

En este caso en vez de abrir `python3` y escribir directamente sobre él órdenes, creamos un fichero y luego le decimos, oye, ábreme esto, se parece más a tener un documento de Word y abrirlo con Word, una pequeña analogía.

