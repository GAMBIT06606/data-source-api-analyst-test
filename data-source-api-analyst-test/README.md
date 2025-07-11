# Data Source API Analyst - GitHub API Homework

## Objetivo del Proyecto

El objetivo de este proyecto es demostrar la capacidad para:

- Comprender la estructura de una API (en este caso, la de GitHub).
- Hacer solicitudes autenticadas a endpoints reales.
- Aplicar paginación, manejo de errores, y almacenamiento de resultados.
- Automatizar la extracción de datos con Python desde Google Colab.

Este ejercicio fue realizado como parte de una evaluación para el rol de **Data Source API Analyst**.

---

## Herramientas Utilizadas

| Herramienta             | Uso principal                                      |
| ----------------------- | -------------------------------------------------- |
| GitHub API              | Fuente de datos (repositorios, commits, contenido) |
| Google Colab            | Desarrollo y ejecución del código Python           |
| Python (requests, json) | Realizar solicitudes y guardar resultados          |

---

## Estructura del Repositorio

```
Data-Source-API-Analyst-Test/
|
├── README.md                    # Este documento explicativo
|
├── Content/
│   ├── github_api_commits.ipynb # Notebook completo con código, funciones y explicaciones
│   └── commits_pandas.json      # Archivo de salida con los commits extraídos
```

---

## Descripción de los Pasos Realizados

### 1. Autenticación

- Se utilizó un token personal para autenticar las solicitudes a la API de GitHub.
- Se configuraron las cabeceras necesarias (`Authorization`, `Accept`, `X-GitHub-Api-Version`).

### 2. Búsqueda de Repositorios

- Endpoint utilizado: `/search/repositories`
- Palabra clave utilizada: `"machine learning"`
- Los resultados se ordenaron por popularidad (`stars`).

### 3. Extracción de Commits con Paginación

- Endpoint utilizado: `/repos/{owner}/{repo}/commits`
- Se implementó una función `get_all_commits()` para recorrer varias páginas (hasta 3).
- Se extrajo información de SHA, autor, mensaje y fecha del commit.

### 4. Consulta de Contenido del Repositorio

- Endpoint utilizado: `/repos/{owner}/{repo}/contents/{path}`
- Se listó el contenido del repositorio `pandas-dev/pandas`.
- Se incluyó un ejemplo en el docstring para explorar subcarpetas.

### 5. Manejo de Errores

- Se incluyó manejo para errores comunes como `401`, `403`, `404`, y fallos de red.
- Se explicó qué hacer en cada caso.

### 6. Exportación de Resultados

- Los commits extraídos fueron almacenados en un archivo `.json` para análisis posterior.


## Reflexión Final

> Este proyecto representa un gran reto personal, ya que es la primera vez que realizo un desarrollo de esta magnitud. Para lograrlo, tuve que estudiar mucho, aprender desde cero varios conceptos técnicos sobre APIs, autenticación, paginación y automatización de datos con Python. Fueron muchas horas de investigación, práctica y ensayo/error. A pesar de que aún hay aspectos que no domino al 100%, me siento satisfecho con el trabajo realizado porque logré avanzar considerablemente, y sobre todo, aprendí muchísimo. Agradezco la oportunidad de haberme enfrentado a este reto, ya que me ha permitido crecer profesionalmente.