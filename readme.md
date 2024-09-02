# Trabajo Practico Curso Data Engineering UTN FRBA

## Parte 1 : Extracción y almacenamiento de datos

### Objetivos
● Implementar técnicas de extracción de datos por medio del lenguaje de programación
Python.</br>
● Implementar técnicas de almacenamiento de datos, con el formato parquet.
### Consigna
Desarrollar un programa en Python que realice:
1. Extracción de una API, como fuente de datos,
2. Convierta los datos obtenidos como DataFrames de Pandas
3. Guarde los datos en forma cruda, sin transformaciones o con leves transformaciones,en formato parquet.
<br>Deberás usar la librería requests para obtener datos de 2 o más endpoints de la misma
API.</br>

<br>Uno de los endpoints debe devolver datos temporales, que se actualicen
periódicamente (mínimo una vez al día), como por ejemplo: valores meteorológicos,
cotizaciones de monedas o acciones de compañías, variaciones de índices económicos,
estadísticas deportivas, etc, El otro endpoint debe ofrecer datos estáticos o
metadatos, como por ejemplo campos o atributos que describen a una estación
meteorológica, a una ciudad, a una empresa o moneda, a un club deportivo, etc.</br>

<br>
Deberás realizar una extracción incremental y una full, según corresponda.
Además tendrás que guardar cada DataFrame en formato parquet, cada uno en un
directorio específico, como si fuese que estás trabajando en un data lake.</br>

<br>En caso de que estés haciendo una extracción incremental, deberás particionar
por cada fecha y también por hora (si corresponde).
</br>
En el caso de datos relativamente estáticos, podes particionar. O no, por algún
otro campo, si consideras necesario.

## Parte 2 : Procesamiento de datos
### Objetivos
● Implementar técnicas para procesamiento para limpiar y estandarizar los datos.</br>
● Aplicar técnicas de procesamiento para enriquecer los datos y obtener información
relevante.
### Consigna
En la consigna anterior, has guardado datos crudos en formato Parquet.
Ahora, deberás leer esos archivos y aplicar tareas de procesamiento o transformación
de datos con Pandas. Esas tareas de procesamiento pueden ser:
- Eliminación de duplicados
- Eliminación o reemplazo de nulos
- Conversión de tipos de datos de columnas
- Renombrar columnas
- Formatear columnas de tipo fecha.
- Crear nuevas columnas a partir de alguna lógica (Por ejemplo, una columna
booleana que indique si una temperatura está por arriba de un límite)
- Cruzar dataframes usando JOINS
- Aplicar agregaciones por medio de GROUP BY y funciones como MAX, MIN,
AVG, etc.</br>

Deberás realizar al menos 4 tareas de transformación.
El resultado del procesamiento debe ser guardado en una, o varias, tablas de una base
de datos OLAP, Cabe aclarar que tenés que realizar la creación de las tablas desde
Python con la librería SQLAlchemy
