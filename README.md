# Tasa de suicidios entre los años 1985 al 2016
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Suicidio.jpg)
El presente proyecto consiste en el análisis del DATASET "Suicide Rates Overview 1985 to 2016", haciendo uso de distintos modelos de machine learning para el procesamiento de los datos a travésde la herramienta.

## Obtenido de:
https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016
## Especificación de los campos
* País: Es el país el cuál está siendo objeto de estudio.
* Año: Es el año del cual se tomaron los datos.
* Sexo: Es el genero de las personas analizadas. Este puede ser:
  * Male -> Masculino.
  * Female -> Femenino.
* Rango de edad: Es el rango de edad que se está analizando. Estos pueden ser:
  * 5-14 años.
  * 15-24 años.
  * 25-34 años.
  * 35-54 años.
  * 55-74 años.
  * 75+ años.
* Nro. de suicidios: Es la cantidad de suicidios que se presentaron.
* Población: Es la población existente.
* Suicidios/100k Población: Es el promedio del número de suicidios de cada 100000 personas.
* País-Año: Contiene el país concatenado al año del cuál se está hablando.
* Índice de desarrrollo humano (HDI) por Año: Es un indicador que que mide el nivel de desarrollo de cada país atendiendo a variables como la esperanza de vida, la educación o el ingreso per cápita. El cual ha sido estimado por cada año.
  * Desarrollo humano muy alto, aquellos con niveles superiores al 0,80.
  * Desarrollo humano alto, cuyos niveles rondan entre 0,70 y 0,80.
  * Desarrollo humano medio, cuyos niveles rondan entre 0,50 y 0,70.
  * Desarrollo humano bajo, con una valoración inferior a 0,55.
* Producto interno bruto (GDP) por Año:  Es la suma total del precio en el mercado de todos los bienes y servicios finales producidos por un país durante un período de tiempo fijo, en este caso, un año.
* Generación: Posee la generación a la que pertenece dicho rango de edad. Estos pueden ser:
  * Generación X
  * Generación Z
  * Millenials
  * Boomers
  * G.I. Generation
  * Silent 
## Modelos/Algoritmos a utilizar
### Redes bayesianas
>Las redes bayesianas son una representaci´on gr´afica de dependencias para razonamiento probabilstico, en la cual los nodos representan variables aleatorias
y los arcos representan relaciones de dependencia directa entre las variables. Pueden definirse como un grafo orientado y sin ciclos en el que los nudos
representan variables aleatorias y los arcos que los encadenan expresan las relaciones entre dichas variables. En la red o grafo, cada variable aleatoria recibe la asignación de su probabilidad de comportamiento, así como las probabilidades condicionales correspondientes.

Las redes bayesianas permiten caracterizar diferentes variables y definir la relación entre varios eventos. La mayoría de los problemas y aplicaciones del mundo real son difíciles de resolver. Sin embargo, la naturaleza de esas aplicaciones es probabilística. Por eso necesitamos una solución como una red bayesiana. La red bayesiana también se puede utilizar para las siguientes tareas:
* Tomar decisiones para factores inciertos
* Predicción de series temporales
* Razonamiento
* Diagnóstico
* Predicción
* Conocimiento automatizado
* Detección de anomalías
Al diseñar un gráfico con la ayuda de las redes bayesianas, es necesario medir los nodos y los enlaces entre esos nodos. Estos son los dos componentes que completan una red bayesiana.
### Árbol de decisión
