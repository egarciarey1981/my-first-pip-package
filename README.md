# my-first-pip-package

En Python se usa PIP para utilizar bibliotecas de terceros.

Me he preguntado si sería capaz de crear una biblioteca Python, y he sido capaz.

He utilizado este tutorial: https://packaging.python.org/en/latest/tutorials/packaging-projects/

## Creación

Lo primero que he hecho ha siso crear una carpeta src y dentro una clase Math con 2 métodos (add y sub).

Para que todo el código que hagamos se considere una biblioteca, hay que crear un fichero pyproject.toml e indicar su nombre y versión:

```
[project]
name = "math_egarciarey1981"
version = "0.0.1"
authors = [
  { name="Eliecer García Rey", email="egarciarey1981@gmail.com" },
]
description = "My first Pip Package"
readme = "README.md"
requires-python = ">=3.7"
classifiers = [
    "Programming Language :: Python :: 3",
    "License :: OSI Approved :: MIT License",
    "Operating System :: OS Independent",
]
```

## Instalación

Para instalar la biblioteca, hay que ejecutar el siguiente comando:

```
pip install git+https://github.com/egarciarey1981/my-first-pip-package#egg=math_egarciarey1981
```

## Uso

Como con cualquier otra biblioteca, hay que importarla para poder utilizarla:

```
from math_egarciarey1981.math import Math

math = Math()
result = math.add(1, 2)
```