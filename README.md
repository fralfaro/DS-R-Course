# Curso de R (Template)

![example workflow](https://github.com/fralfaro/DS-R-Course/actions/workflows/documentation.yml/badge.svg)
<a href="https://fralfaro.github.io/DS-R-Course/"><img alt="Link a la Documentación" src="https://img.shields.io/badge/docs-link-brightgreen"></a>


## Descripción del Repositorio

```
|
├───.github
│   └───workflows
│           documentation.yml
│
├────docs
│   ├───.images
│   │       logo.bmp
│   │       logo_r.bmp
│   │
│   │   __init__.py
│   │   basic.ipynb
│   │   dplyr.ipynb
│   │   ggplot2.ipynb
│   │   index.md
│   │   intro.ipynb
│   
│   .gitignore
│   LICENSE
│   mkdocs.yml
│   poetry.lock
│   pyproject.toml
│   README.md
```

donde:

* `documentation.yml`: archivo para generar el CI del proyecto.
* `docs`: carpeta donde se almacenan los jupyter notebooks.
  * `images`: carpeta con las imagenes del *logo* y el *favicon*. 
  * `index.md`: archivo markdown inicial.
  * `*.ipynb`: archivos jupyter notebook.
* `.gitignore`: lugar donde se define los archivos a ignorar.
* `LICENSE`: licencia asociada al proyecto.
* `mkdocs.yml`: archivo que orquestará la documentación del proyecto.
* `poetry.lock`: archivo que orquestará el proyecto y sus dependencias.
* `pyproject.toml`: archivo que orquestará el proyecto y sus dependencias.
* `README.md`: archivo que describe el repositorio.

## Github Settings 

### Actions

1. Ir a `Settings -> Actions -> General`.

<img src="https://drive.google.com/uc?export=view&id=1JedsyCEC3GYj7k0dGD7w0DoS1PQ3Lr5W" width = "600" align="center"/>

2. Marcar las opciones como se muestra en la imagen y guardar sus cambios.

<img src="https://drive.google.com/uc?export=view&id=1vQPUAJ0fHiqt3L-4uue3QgJF6C2vQZL1" width = "500" align="center"/>

### Pages 

1. Ir a `Settings -> Pages -> GitHub Pages`.
2. Marcar las opciones como se muestra en la imagen y guardar sus cambios.

<img src="https://drive.google.com/uc?export=view&id=1QW8oLwRg1VmjInyeA6DCWo6Hv8znGtE_" width = "600" align="center"/>

> **Nota**: Primero debe realizar los cambios en `Actions`, realizar un `git push` (de algún archivo) para habilitar esta opción correctamente.

## Archivos a modificar

### [Readme.md](README.md)

```
![example workflow](https://github.com/fralfaro/DS-R-Course/actions/workflows/documentation.yml/badge.svg)
<a href="https://fralfaro.github.io/DS-R-Course/"><img alt="Link a la Documentación" src="https://img.shields.io/badge/docs-link-brightgreen"></a>
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-R-Course**: nombre del curso.

### [`mkdocs.yml`](mkdocs.yml)

**Sección**: Project information - Repository

```
# Project information
site_name: Home
site_url: https://github.com/fralfaro/DS-R-Course
site_author: Francisco Alfaro
site_description:

# Repository
repo_name: fralfaro/DS-R-Course
repo_url: https://github.com/fralfaro/DS-R-Course
edit_uri: ''
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-R-Course**: nombre del curso.
* **site_author**: Nombre del autor

**Sección**: Theme

```
# Theme
theme:
  name: material
  language: es
  logo: images/logo.bmp
  favicon: images/logo_r.bmp
```
Debe cambiar:

* **favicon**: imagen a utilizar como *favicon*.

**Sección**: Customization

```
# Customization
extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/fralfaro
    - icon: fontawesome/brands/linkedin
      link: https://www.linkedin.com/in/faam/
    - icon: fontawesome/solid/globe
      link: https://fralfaro.github.io/portfolio/
```
En esta sección se agregan las redes sociales 
que ustedes maneja (más detalles, 
ver el siguiente [link](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/#with-animations)).

**Sección**: TOC

```
# TOC
nav:
    - Home: index.md
    - Conceptos Básicos:
        - intro.ipynb
        - basic.ipynb
    - Manipulación Datos:
        - dplyr.ipynb
        - ggplot2.ipynb
```

En esta sección se agregan los archivos `.ipynb` que necesita agregar a su documentación.

### Otros

#### [`pyproject.toml`](pyproject.toml)

```
[tool.poetry]
name = "docs"
version = "0.1.0"
description = "mkdocs - courses"
authors = ["Francisco Alfaro <francisco.alfaro.496@gmail.com>"]
license = "MIT"
readme = "README.md"
```

Cambiar `authors` por su nombre y correo personal.

#### [`index.md`](docs/index.md)

```
# Introducción básica a R

## Material

El material está disponible en el siguiente [repositorio](https://github.com/fralfaro/DS-R-Course), para obtener el código de fuente basta con que ejecutes el siguiente comando:

```
https://github.com/fralfaro/DS-R-Course
```

## Contenidos temáticos

* Introducción a R
* Nomenclatura
* Introducción dplyr
* Introducción ggplot2
```

Debe cambiar:

* **fralfaro**: nombre de usuario en github.
* **DS-R-Course**: nombre del curso.


> **Nota**: Si necesita customizar su repositorio, se recomienda leer el siguiente [link](https://squidfunk.github.io/mkdocs-material/).

## Recomendaciones

Para efectos prácticos, se recomienda tener sus datos (*datasets* e *imágenes*) en **Google Drive**, 
en donde tenga la información separada en dos carpetas:
* `datasets`: carpeta con los datasets del curso.
* `images`: carpeta con las imágenes del curso.

> **Nota**: Ver la siguiente [carpeta](https://drive.google.com/drive/folders/19pXxciBMm7aSgz72tA-X7BT0q677DEmd?usp=sharing) a modo de ejemplo.

<img src="https://drive.google.com/uc?export=view&id=1J17-gO4PD5WBDe0u1bLtNrEq8MpM5B7q" width = "300" align="center"/>

Debe habilitar la opción `Share -> General access -> Anyone whit the link`, para que otras personas pudan leer 
los datasets y las imágenes de su carpeta.

<img src="https://drive.google.com/uc?export=view&id=1HJOBh3jx4L-YX-o2abygTu3XOQdF5HSB" width = "300" align="center"/>

1. En Jupyter notebook, para mostrar una imagen, se utiliza la siguiente sequencia:

```markdown
<img src="https://drive.google.com/uc?export=view&id=<ID_IMAGE>" width = "300" align="center"/>
```

donde `<ID_IMAGE>` corresponde al id de su imagen a compartir desde Google Drive.

2. En Jupyter notebook, para leer un dataframe con `pandas`, se utiliza la siguiente sequencia:

```python
import pandas as pd

url='<URL_DATASET>'
url='https://drive.google.com/uc?id=' + url.split('/')[-2]

df = pd.read_csv(url, sep="," )
```

donde `<URL_DATASET>` corresponde a la URL de su dataset a compartir desde Google Drive.
