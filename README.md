<h1 align="center">  Análisis del número de accidentes de tráfico del año 2015 en Estados Unidos </h1>

El siguiente repositorio se realiza un análisis del número de accidentes de tráfico del año 2015 en Estados Unidos, utilizando el dataset 'nhtsa_traffic_fatalities' del proyecto 'bigquery-public-data', utilizando BigQuery y Python.


## Objetivos
_Para este análisis se solicitan realizar las siguientes instrucciones:_
1. Crear y completar un diccionario de datos de la tabla, guardarlo en un archivo de texto separado por comas `.csv`
Lo siguiente se debe realizar en un jupyter notebook.
2. Identificar, usando consultas y con gráficas las siguientes características del dataset.
   1. Mayor número de accidentes por estado.
   2. Mayor número de accidentes por uso de tierra.
   3. Mayor número de accidentes por empresa de carreteras.
   4. Mayor número de accidentes por carretera.
3. Realizar un análisis mensual de accidentes por estado.
4. Realizar un análisis según la hora del dia.
   - Ahondar para los estados con mayor cantidad de muertes
5. Finalmente realizar un análisis resaltando la razón entre números de accidentes y conductores ebrios.

## Pregunta 1
Para la pregunta 1, se generó el siguiente archivo 'csv' con el [diccionario de datos](diccionario_de_datos.csv)

## Pregunta 2.1: Mayor número de accidentes por estado

Se puede notar que el mayor número de accidentes se produjeron en el estado de Texas con 3190 accidentes, lo siguen California con 3123 y Florida con 2699, estos 3 estados destacan en gran proporción sobre el resto.

[![accidentes-2015.png](https://i.postimg.cc/C1Bqk1YY/accidentes-2015.png)](https://postimg.cc/9R20jcrN)
_El gráfico muestra los estados con la mayor cantidad de accideentes de tránsito en Esstados Unidos en el año 2015._

## Pregunta 2.2: Mayor número de accidentes por uso de tierra

Se cuentan la cantidad de accidentes que se dieron en sectores rurales y urbanos.  
Se puede notar que los accidentes urbanos son los que ocurren con más frecuencia, aunque no por mucho, es aproximadamente un 4% mayor que los accidentes rurales.

[![rural-urbano.png](https://i.postimg.cc/1zqfWdn1/rural-urbano.png)](https://postimg.cc/hJKDvp12)
_El gráfico muestra la cantidad de accidentes en los lugares rurales y los lugares urbanos._

## Pregunta 2.3: 