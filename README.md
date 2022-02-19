# Tasa de suicidios entre los años 1985 al 2016
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Suicidio.jpg)
El presente proyecto consiste en el análisis del DATASET "Suicide Rates Overview 1985 to 2016", haciendo uso del algoritmo de machine learning "Redes bayesianas" para el procesamiento de los datos a través de la herramienta Weka.
## Descripción del Dataset
Consiste en el número de suicidios que se han presentado a nivel mundial a través de los años 1985 hasta el 2016. El mismo consta de 12 atributos (los cuáles se describirán posteriormente), y un total de 27820 instancias.
## Obtenido de:
https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016
## Especificación de los atributos
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
>Las redes bayesianas son una representación gráfica de dependencias para razonamiento probabilstico, en la cual los nodos representan variables aleatorias
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
#### Procedimiento
1. Se carga el dataset (Archivo .csv) en el programa Weka haciendo click en "Open File".
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/1.PNG)
2. Se selecciona el filtro supervisado llamado "Discretización" y se hace click en "Apply".
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/2.PNG)
3. 1) Se dirige a la parte de "Classify", 2) se busca el algoritmo de clasificación "BayesNet", 3) luego se selecciona la opción "Use training set", 4) posteriormente se escoge el campo principal, el cual será la cabeza o base para visualizar el porcentaje, y 5) finalmente se hace click en "Start". 
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/3.PNG)
4. El resultado que nos dará es el siguiente:
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/4.PNG)
5. Luego, para poder visualizar el grafo resultante, se hace click derecho sobre el modelo obtenido y se selecciona la opción "Visualize graph".
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/5.PNG)
6. Aquí se nos presentará el gráfico con el atributo que seleccionamos como raíz, y los demás atributos que se derivan de este.
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/6.PNG)
7. Finalmente, si se quiere visualizar los porcentajes de las relaciones entre dos atributos de la tabla, se hace click en cuálquiera de los nodos, y se presentará una tabla como la que se muestra a continuación:
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Pasos/Redes_bayesianas_primer_modelo/7.PNG)

#### Resultados obtenidos
##### Red bayesiana del DATASET
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Redes_Bayesianas/Redes_bayesianas_principal.PNG)
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
### Redes Bayecianas del DATASET (REDUCIDO)
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasCountry.png)

### Resumen
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResumenInstancias.png)
En este caso de entrenamiento del modelo, se lo hizo en base a la variable "Country" del dataset reducido ya que con esta variable se conseguía aumentar la cantidad de instancias correctamente clasificadas llega al 99% en comparación al 65% del primer modelo.
### Matriz de confusión
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/MatrizConfunsiónA.png) 
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/MatrizConfunsiónB.png)
### Sexo
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorSexo.png)
### Generación
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorGeneracion.png)
### Año
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorAño.png)
### Edad
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorEdad.png)
### GDP
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasGDP_per_capita.png)
### HDI
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/redesBayecianasHDI.png)
### Población
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorPoblacion.png)
### Población / 100K
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPor100K.png)
### NRro. Suicidios
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/resultadosDatosDividos/ResultadosPorNroSuicidios.png)
## Comparación de Algoritmos
|Algoritmo|Porcentaje de instancias correctamente clasificadas|Instancias correctas|Instancias incorrectas|
|---:|:---:|---:|:---:|
|Redes Bayecianas|65.3559 %|18182|9638|
|Simplekmeans|68.6403 %|74.5389 |74.5389 |
|J48|| ||
|DecisionStump|32.1208 %|8936|18884|
|RandomTree|72.5306%|20178|7642|
|RandomProjection|72.5306%|20178|7642|
|ZeroR|23.0338%|6408|21412|
## Predicción de los Datos
Para esta seccion se dividió en dos partes el dataset, 80% para el entrenamiento del modelo mediante Redes bayesianas, y 20% para la predicción. Una vez creado el modelo, se hizo uso del mismo para realizar el respectivo test de predicciones, mediante la cual se pudo obtener los siguientes resultados:
* Predicción por año
Se puede visualizar a continuación que a partir de los años 2005 al 2006 es posible que exista un aumento de suicidios en los distintos países.\
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Prediccion/PrediccionYear.png)

* Prediccion por Pais
Se puede visualizar a continuación que en los países de Argentina, Slovakia y Antigua and Barbuda pueden aumentar los casos de suicidios.\
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Prediccion/PrediccionCounter.png) 

* Prediccion por Generacion
Se puede visualizar a continuación que la "Generación X" es la más propensa a suicidarse a lo largo de todos los países.\
![Image text](https://github.com/alexisdquizhpe/AnalisisDataSet_IA/blob/main/Imagenes/Prediccion/PrediccionGeneracion.png) 

## Bibliografía

Data Science. 2021. Redes Bayesianas. [online] Available at: <https://datascience.eu/es/matematica-y-estadistica/redes-bayesianas/> [Accessed 18 February 2022].
Yates, R. 2019. https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016. [online] Available at: <https://www.kaggle.com/russellyates88/suicide-rates-overview-1985-to-2016> [Accessed 18 February 2022].
