# Data Cleaning and Analysis - Movies Dataset 🎈🎦

 Por: Manuela Botero Buitrago

 
Este proyecto se centra en la limpieza y transformación de un conjunto de datos de películas. El objetivo principal fue realizar el "data wrangling" del dataset, lo que incluyó la eliminación de valores nulos, el tratamiento de columnas con datos inconsistentes, la transformación de valores y la creación de nuevas columnas útiles para análisis posteriores.

El dataset utilizado contiene información sobre películas y programas de televisión, con columnas como "MOVIES", "YEAR", "GENRE", "RATING", "ONE-LINE", "STARS", "VOTES", "RUNTIME" y "GROSS".

## Pasos Realizados

A continuación se detallan los principales pasos realizados en el notebook:

### 1. **Carga de Datos**
   - El dataset original se cargó desde un archivo CSV utilizando `pandas`.

### 2. **Exploración Inicial**
   - Se inspeccionaron las primeras filas del dataset para entender la estructura y el tipo de datos presentes.
   - Se verificaron los tipos de datos y se identificaron las columnas con valores nulos.

### 3. **Limpieza de Datos**
   - **Eliminación de caracteres no deseados en la columna `Year`:**
     - Se eliminaron los paréntesis de la columna `Year` utilizando `str.replace()`.
   - **Relleno de valores nulos en la columna `Year`:**
     - Se utilizaron varios métodos de relleno para los valores nulos en la columna `Year`, como el relleno hacia adelante (`ffill`) o con un valor predeterminado.
   - **Separación de columnas:** 
     - En la columna `STARS`, se separaron los nombres de los directores y actores utilizando `str.split()`.
   - **Eliminación de columnas irrelevantes:**
     - Se eliminaron las columnas no necesarias, como `Gross`, para centrarse en las variables de interés.

### 4. **Transformación de Datos**
   - Se realizaron transformaciones en las columnas de texto, como la eliminación de saltos de línea (`\n`).
   - Se separaron los valores compuestos en la columna `STARS` en dos nuevas columnas: `DIRECTOR` y `ACTORS`.

### 5. **Filtrado de Datos**
   - Se realizaron filtros para eliminar o ajustar registros donde los valores de la columna `Year` eran desconocidos o faltaban.

### 6. **Guardado del Dataset Limpio**
   - El dataset limpio se guardó en un nuevo archivo CSV con el nombre `movies_cleaned.csv` para su uso en análisis posteriores.

## Resultados Esperados

Después de realizar la limpieza de los datos, el dataset estará listo para un análisis más profundo o para ser utilizado en modelos de recomendación, análisis de tendencias en películas, o cualquier otro análisis relevante.

 
