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
#### Resultados obtenidos
##### Red bayesiana del DATASET
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Redes_bayesianas_principal.PNG)\
##### Resumen
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Resumen.PNG)\
En base a la imagen se puede observar que el 65.36% de los datos fue clasificado correctamente, es decir 18182 instancias de un total de 27820. 
##### Matriz de confusión
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Matriz_confusion.PNG)\
Con los resultados obtenidos en la matriz de confusión se puede observar que los valores de la diagonal son los de mayor valor, por ende los resultados son validos.
##### Sexo
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Sexo.PNG)\
En base a la imagen se puede observar que el sexo que más tiende a tomar la decisión de suicidarse es el masculino.
##### Generación
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Generacion.PNG)\
En base a la grafica la generación que más tiende al suicidio son los llamados "Boomers" con un porcentaje de 87.5%
##### Año
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Anio.PNG)\
En base a la imagen, el rango de los años en los que más gente se suicidó fue de 1994 al 2006.
##### Edad
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Edad.PNG)\
El rango de edad que más tiende al suicidio es de 35 a 54 años.
##### GDP
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/GDP.PNG)\
En base a la gráfica, se puede observar que en los paises donde existe un menor PIB es donde más suelen suicidarse las personas.
##### País
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pais.PNG)\
En base a la gráfica, se puede observar que el país que más índices de suicidio ha tenido es Rusia.

## Resultados de la división de los datos
Tomando en cuenta que la cantidad de arreglos o filas que existian en el archivo .csv es de 28 mil aproximadamente, se procedio a dividirlos en dos archvios, con el fin de contar con dos datasets que contengan la misma estructura, pero que el de mayor cantidad de arreglos sirva para el entrenamiento del modelo, y el archivo restante para la puesta en práctica del modelo entrenado.
#### Redes Bayecianas del DATASET (REDUCIDO)
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasCountry.png)
#### RESUMEN
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResumenInstancias.png)
#### MATRIZ DE CONFUSÓN 
=== Confusion Matrix ===

   a   b   c   d   e   f   g   h   i   j   k   l   m   n   o   p   q   r   s   t   u   v   w   x   y   z  aa  ab  ac  ad  ae  af  ag  ah  ai  aj  ak  al  am  an  ao  ap  aq  ar  as  at  au  av  aw  ax  ay  az  ba  bb  bc  bd  be  bf  bg  bh  bi  bj  bk  bl  bm  bn  bo  bp  bq  br  bs  bt  bu  bv  bw  bx  by  bz   <-- classified as
 264   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   a = Albania
   0 324   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   b = Antigua and Barbuda
   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   c = Argentina
   0   0   0 298   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   d = Armenia
   0   0   0   0 168   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   e = Aruba
   0   0   0   0   0 358   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   f = Australia
   0   0   0   0   0   0 382   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   g = Austria
   0   0   0   0   0   0   0 190   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   h = Azerbaijan
   0   0   0   0   0   0   0   0 276   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   i = Bahamas
   0   0   0   0   0   0   0   0   0 252   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   j = Bahrain
   0   0   0   0   0   0   0   0   0   0 299   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   k = Barbados
   0   0   0   0   0   0   0   0   0   0   0 251   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   l = Belarus
   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   m = Belgium
   0   0   0   0   0   0   0   0   0   0   0   0   0 336   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   n = Belize
   0   0   0   0   0   0   0   0   0   0   0   0   0   0  23   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   o = Bosnia and Herzegovina
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 371   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   p = Brazil
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 349   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  10   0   0   0   0   0   0   0   0   0   0   0   0 |   q = Bulgaria
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  11   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   r = Cabo Verde
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 347   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   s = Canada
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 368   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   3   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   t = Chile
   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 369   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   u = Colombia
   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0 351   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   6 |   v = Costa Rica
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 262   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   w = Croatia
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0 286   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |   x = Cuba
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 176   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2 |   y = Cyprus
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 321   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0 |   z = Czech Republic
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 264   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  aa = Denmark
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  12   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ab = Dominica
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ac = Ecuador
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 284   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   1   0   0   0   0   1   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ad = El Salvador
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 252   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ae = Estonia
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 132   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  af = Fiji
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 348   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ag = Finland
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 360   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ah = France
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0 262   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ai = Georgia
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 312   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  aj = Germany
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 371   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ak = Greece
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 310   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  al = Grenada
   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 357   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  am = Guatemala
   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 297   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  an = Guyana
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 309   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0 |  ao = Hungary
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 382   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ap = Iceland
   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 359   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  aq = Ireland
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 371   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ar = Israel
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  as = Italy
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 201   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0 |  at = Jamaica
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  au = Japan
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0 311   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  av = Kazakhstan
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 132   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  aw = Kiribati
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 299   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ax = Kuwait
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 312   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ay = Kyrgyzstan
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 252   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  az = Latvia
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 261   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  ba = Lithuania
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bb = Luxembourg
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  11   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bc = Macau
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0 119   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bd = Maldives
   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 371   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  be = Malta
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 381   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1 |  bf = Mauritius
   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 370   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0 |  bg = Mexico
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   9   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bh = Mongolia
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0 118   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bi = Montenegro
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 382   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bj = Netherlands
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 348   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bk = New Zealand
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  72   0   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bl = Nicaragua
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0 356   0   0   0   0   0   0   0   0   0   0   0   0   0 |  bm = Norway
   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  34   0   0   0   0   0   0   0   0   0   0   0   0 |  bn = Oman
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 299   0   0   0   0   0   0   0   0   0   0   1 |  bo = Panama
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   2   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0 321   0   0   0   0   0   0   0   0   0   0 |  bp = Paraguay
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0 179   0   0   0   0   0   0   0   0   0 |  bq = Philippines
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   1   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 285   0   0   0   0   0   0   0   0 |  br = Poland
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 323   0   0   0   0   0   0   0 |  bs = Portugal
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0   0   0 |  bt = Puerto Rico
   0   3   0   0   1   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 173   0   0   0   0   0 |  bu = Qatar
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 372   0   0   0   0 |  bv = Republic of Korea
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 333   0   0   0 |  bw = Romania
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   1   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 323   0   0 |  bx = Russian Federation
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0  36   0 |  by = Saint Kitts and Nevis
   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0 145 |  bz = Saint Lucia
#### SEXO
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorSexo.png)
#### GENERACIÓN
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorGeneracion.png)
#### AÑO 
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorAño.png)
#### EDAD
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorEdad.png)
#### GDP
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasGDP_per_capita.png)
#### HDI
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasHDI.png)
#### POBLACIÓN
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorPoblacion.png)
#### POBLACIÓN / 100K
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPor100K.png)
#### NRO. SUICIDIOS
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorNroSuicidios.png)
## Comparación de Algoritmos
|Algoritmo|Total Instancias correctamente clasificadas|Instancias correctamente clasificadas|Instancias Incorrectas|
|---:|:---:|---:|:---:|
|__Tipo_|_Trees__|__Sucess_|_Fail__|
|Redes Bayecianas|65.3559 %|18182|9638|
|Simplekmeans|68.6403 %|74.5389 |74.5389 |
|J48|| ||
|DecisionStump|32.1208 %|8936|18884|
|RandomTree|72.5306%|20178|7642|
|RandomProjection|72.5306%|20178|7642|
|ZeroR|23.0338%|6408|21412|
