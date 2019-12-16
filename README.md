# Análisis de estadística espacial para el Índice de Desarrollo Social Cantonal de Costa Rica.

## Resumen
Este repositorio contiene el código y datos de la presentación sobre el proyecto 4 del curso SP-1649 Tópicos de Estadística Espacial Aplicada: El titulo del repositorio es **Análisis de estadística espacial para el Índice de Desarrollo Social Cantonal de Costa Rica.**, desarrollado por Melissa Cordero Díaz y Marco Otoya Chavarría, como parte de la Maestría en Estadística de la Universidad de Costa Rica.


- [Análisis de estadística espacial para el Índice de Desarrollo Social Cantonal de Costa Rica.](#Análisis-de-estadística-espacial-para-el-Índice-de-Desarrollo-Social-Cantonal-de-Costa-Rica.)
  - [Resumen](#resumen)
  - [Estructura del repositorio](#estructura-del-repositorio)
  - [Datos](#datos)
    - [Fuentes de información](#fuentes-de-información)
    - [Descripción de los datos](#descripción-de-los-datos)
    - [Detalle de las variables](#detalle-de-las-variables)
  - [Análisis](#análisis)
  - [Gráficos y mapas](#gráficos-y-mapas)
  - [Preguntas](#preguntas)
  
  ## Estructura del repositorio

El repositorio está compuesto por un archivos de R, usado para realizar el análisis y tres carpetas que contienen los datos, los gráficos producidos y la presentación y el reporte final:

- Los archivos de R, disponibles en formato `.R`, contine el analisis exploratorio de los datos, la aplicación de los criterios utilizados para la matriz de pesos, el análisis de autocorrelación espacial, la aplicación de los modelos de regresión lineal, CAR y SAR. (`IDS_Cant_Traba_Final.R`)

- La carpeta `Datos` contiene los datos usados, la carpeta `Plots` contiene los gráficos y mapas producidos y usados en el artículo, y finalmente la carpeta `Reporte` contiene la presentación y el documento final.

## Datos

### Fuentes de información

Se cuenta con los datos del IDS cantonal del MIDEPLAN para el 2017, así como sus dimensiones. Así mismo, se utilizó información del INEC para algunas de las covariables utilizadas. Los datos del IDS descargarse directamente del siguiente link:

Datos de IDS: https://www.mideplan.go.cr/indice-desarrollo-social

### Descripción de los datos

Los datos disponibles del IDS cantonal y las covariables utilizadas se encuentran para ada uno de los 82 cantones del país, además se utilizó un archivo shape de los cantones de Costa Rica para realizar el análisis de áreas.

### Detalle de las variables

Dado que el IDS se construye a partir de sus dimensiones, las dimensiones del índice no se consideran para el análisis.  De manera alternativa se utilizan variables de tipo socioeconómicas y disponibles para los cantones, entre ellas, el porcentaje de hogares con acceso a internet, la población por cantón y la severidad de pobreza, obtenidas del Instituto Nacional de Estadística y Censos, adicionalmente, se consideró el consumo se de energía eléctrica por cantón, cuyos datos fueron obtenidos de la Autoridad Reguladora de los Servicios Públicos (Aresep).

### Flujo de trabajo
La presente investigación consideró el siguiente análisis:
a.	Análisis gráfico del índice de desarrollo social para el país.
b.	Creación de la base de datos y unión con el archivo “shape” de Costa Rica para los cantones.
c.	Determinación de criterios con el propósito de definir vecinos para los cantones de Costa Rica a nivel del IDS.
d.	Selección de la una matriz de pesos para el modelado espacial.
e.	Análisis de la correlación espacial mediante el test de la I de Moran.
f.	Análisis de conglomerados por medio gráfico para el IDS.
g.	Modelar el IDS mediante un modelo de regresión lineal simple.
h.	Modelar el IDS incorporando el componente espacial mediante modelos SAR y CAR
i.	 Realizar una comparación entre modelos para seleccionar el que mejor se ajusta al fenómeno que se desea explicar.


## Análisis

El análisis de los datos se describe en el archivo ` IDS_Cant_Traba_Final.R` y el artículo vinculado al repositorio.

De forma resumida, los análisis consisten en realizar un análisis de estadística espacial de áreas aplicado al Índice de Desarrollo Social Cantonal de Costa Rica, 2017; el índice permite ordenar los distritos según su nivel de desarrollo social. Para el análisis se utilizaron variables socio económicas estimando un modelo de regresión lineal y comparándolos con la estimación de un modelo CAR y SAR.

Se inicia con un análisis exploratorio de los datos visualizando el IDS por cantón del país, para posteriormente definir el método de distancia a utilizar para el respectivo análisis de autocorrelación espacial. Adicionalmente, se compara un modelo de regresión lineal con un modelo CAR y SAR que incluye el componente espacial.

## Gráficos y mapas

Las figuras/mapas estan contenidos en la carpeta `Plots` son generados mediante los comandos del script `IDS_Cant_Traba_Final.R`, con base en los datos del archivo de Excel `IDSCantonSINRC.xls`. Estas figuras estan incluidos en el documentos final con los mismos nombres seguidamente anotados:

- `Figura 1.jpg`: IDS por canton
- `Figura 2.jpg`: Criterio torre
- `Figura 3.jpg`: Critero Reina
- `Figura 4.jpg`: Criterio Vecinos
- `Figura 5.jpg`: Matriz de estilos
- `Figura 6.jpg`: I Moran scatterplot
- `Figura 7.jpg`: Patrones Geográficos de Clusterización
- `Figura 8.jpg`: Moran Local
- `Figura 9.jpg`: Modelacion del IDS residuos
- `Figura 10.jpg`:Residuos modelo SAR
- `Figura 11.jpg`: Residuos modelo CAR

## Preguntas

Cualquier pregunta o puede escribirle a los autores y dueños de este repositorio a las siguientes direcciones de correo electrónico:

- Melissa Cordero Díaz: cmeli-2@hotmail.com
- Marco Otoya Chavarría: marco.otoya.chavarria@una.ac.cr
