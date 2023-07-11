# my-first-pip-package

En Python se usa PIP para utilizar bibliotecas de terceros.

Me he preguntado si sería capaz de crear una biblioteca Python, y he sido capaz.

He utilizado este tutorial: https://packaging.python.org/en/latest/tutorials/packaging-projects/

**NOTA:** Si quieres ver otra forma, en mi opinión, más sencilla, mira mi repositorio [my-second-pip-package](https://github.com/egarciarey1981/my-second-pip-package).

## Creación

Lo primero que he hecho ha siso crear una carpeta *src* y dentro una clase *Math* con 2 métodos (*add* y *sub*).

Para que todo el código que hagamos se considere una biblioteca, hay que crear un fichero *pyproject.toml* e indicar su nombre y versión. Lo de *build-system* parece necesario para que PIP sepa como construir el paquete.

```toml
[project]
name = "math_egarciarey1981"
description = "My first Pip Package"
version = "0.0.1"
requires-python = ">=3.7"

[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"
```



## Instalación

En el servidor donde queramos instalar la biblioteca, hay que ejecutar el siguiente comando:

```bash
pip install git+https://github.com/egarciarey1981/my-first-pip-package
```

Comprobar que se ha instalado correctamente:

```bash
pip list | grep math_egarciarey1981
```

## Uso

Como con cualquier otra biblioteca de tercero, hay que importarla para poder utilizarla:

```python
from math_egarciarey1981.math import Math

math = Math()
result = math.add(1, 2)
```
