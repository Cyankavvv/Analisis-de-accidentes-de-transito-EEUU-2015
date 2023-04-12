<h1 align="center"> Análisis del número de accidentes de tráfico del año 2015 en Estados Unidos</h1>

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
   - Ahondar para los estados con mayor cantidad de muertes.
5. Finalmente realizar un análisis resaltando la razón entre números de accidentes y conductores ebrios.

## Pregunta 1: Crear un diccionario de datos
Para la pregunta 1, se generó el siguiente archivo '.csv' con el [diccionario de datos](diccionario_de_datos.csv)

## Pregunta 2.1: Mayor número de accidentes por estado.

Se puede notar que el mayor número de accidentes se produjeron en el estado de Texas con 3190 accidentes, lo siguen California con 3123 y Florida con 2699, estos 3 estados destacan en gran proporción sobre el resto.

[![accidentes-2015.png](https://i.postimg.cc/C1Bqk1YY/accidentes-2015.png)](https://postimg.cc/9R20jcrN)
_El gráfico muestra los estados con la mayor cantidad de accidentes de tránsito en Esstados Unidos en el año 2015._

## Pregunta 2.2: Mayor número de accidentes por uso de tierra.

Se cuentan la cantidad de accidentes que se dieron en sectores rurales y urbanos.  
Se puede notar que los accidentes urbanos y rurales ocurren casi con la misma frecuencia.

[![graficocircular.png](https://i.postimg.cc/VLM48FnC/graficocircular.png)](https://postimg.cc/9rmyPZxm)

_El gráfico muestra la cantidad de accidentes en los lugares rurales y los lugares urbanos._

## Pregunta 2.3: Mayor número de accidentes por empresa de carreteras.

Se observa que la empresa 'State Highway Agency' presenta el mayor número de accidentes de todas las empresas de carreteras, lo que podría indicar un problema con dicha empresa. Sin embargo, para tener un análisis más completo, es necesario considerar el largo de las carreteras de cada empresa. Es posible que 'State Highway Agency' tenga la mayor cantidad de carreteras en Estados Unidos, por lo que su número de accidentes podría ser proporcionalmente menor en comparación con otras empresas.  

Por otro lado, se puede destacar que hay un número importante de accidentes en los cuales no se reporta o es desconocida la carretera donde fue el accidente.

[![carreteras.png](https://i.postimg.cc/7ZYxGWMn/carreteras.png)](https://postimg.cc/LnwdGvWJ)

_El gráfico muestra la cantidad de accidentes por empresa de carreteras._  

## Pregunta 2.4: Mayor número de accidentes por carretera.

Se logra identificar que la carretera con mayor número de accidentes es la carretera 'I-10'.

[![nombrecarreteras.png](https://i.postimg.cc/qMrB0RNY/nombrecarreteras.png)](https://postimg.cc/23HN7CFF)

_El gráfico muestra la cantidad de accidentes por carretera._


## Pregunta 3: Realizar un análisis mensual de accidentes por estado.

Se puede apreciar que Florida, California y Texas concentran la mayor parte de los accidentes durante todos los meses del año. Curiosamente, en diciembre estos 3 estados suelen tener una cantidad de accidentes muy similar.

[![accidentesa-o.png](https://i.postimg.cc/kg17xvT3/accidentesa-o.png)](https://postimg.cc/4YcCGVCB)

_El gráfico muestra la cantidad de accidentes por cada mes del año 2015, se muestran los estados con mayor cantidad de accidentes._

## Pregunta 4: Realizar un análisis según la hora del día.

Se puede notar un peak importante entre las 17:00 y las 21:00. El cual podría deberse a que en ese horario las personas suelen regresar a sus hogares después del trabajo, por lo tanto hay mucho tráfico y las personas están cansadas. Además, la luz disminuye a esas horas, por lo cual es más fácil que los conductores no vean alguna señal de tránsito, a otros vehículos o peatones.


[![accidenteshorass.png](https://i.postimg.cc/Fstb42Xz/accidenteshorass.png)](https://postimg.cc/hhrQ8ZjR)
_El gráfico muestra la cantidad de accidentes por cada hora del día en el año 2015._

Luego, profundizando para lo estados con mayor cantidad de accidentes:  

[![accidenteshoras.png](https://i.postimg.cc/X7gjvbFv/accidenteshoras.png)](https://postimg.cc/jLL08BMV)
_El gráfico muestra la cantidad de accidentes por cada hora del día en el año 2015, para los estados con mayor cantidad de accidentes_


## Pregunta 5: Realizar un análisis de la razón entre números de accidentes y conductores ebrios
Para obtener esta razón se dividen el número de conductores ebrios por el número de accidentes.

Se decide realizar un análisis de esta razón entre accidentes y conductores ebrios para los estados donde fue el accidente, la hora del día en la cual fue el accidente, y el día de la semana en el cual sucedió el accidente.

En cuanto a los estados, se puede observar que Maine es donde esta relación es mayor, con un 50% de los accidentes que involucran conductores ebrios presentes.

[![aa.png](https://i.postimg.cc/P5t3Y70b/aa.png)](https://postimg.cc/xc43S6fq)
_El gráfico muestra los estados donde la relación conductores ebrios / accidentes es mayor._  

También es útil visualizarlos de manera geográfica, aquí se puede ver que los estados de más al norte presentan una relación mayor entre conductores ebrios y accidentes.
[![mapacalor.png](https://i.postimg.cc/prpch5Sw/mapacalor.png)](https://postimg.cc/tnGN8Jpk)
_El gráfico muestra un mapa de calor de la relación conductores ebrios / accidentes, en Estados Unidos._

Para la hora del día, se puede notar que la razón de 'accidentes / conductores ebrios' es mayor en las horas de la noche y madrugada, tal vez puede explicarse a que a esas horas la gente suele ir a fiestas o volver a sus casas luego de una fiesta, donde es común consumir bebidas alcohólicas.
[![razonhora.png](https://i.postimg.cc/rs18x6PQ/razonhora.png)](https://postimg.cc/0KNR14xw)
_El gráfico muestra la relación conductores ebrios / accidentes para cada hora del día._

Para los días de la semana, se logra notar que los fines de semana es cuando más aumenta la razón, lo que puede explicarse a que son los días de esparcimiento de las personas por lo que suelen consumir bebidas alcohólicas.

[![razonsemana.png](https://i.postimg.cc/SRFSnQDn/razonsemana.png)](https://postimg.cc/Q9mGPDLD)
_El gráfico muestra la relación conductores ebrios / accidentes para cada día de la semana._
