# Proyecto 8

## Grupo b 

### Clustering y visualizacion de curvas de luz de estrellas periódicas

Estudiantes: Macarena Ríos y Melanie Peña

Ayudante: Rafael de la Sotta Vargas

Este proyecto consiste en la clasificación de las caracteristicas obtenidas a partir de las curvas de luz de las estrellas periodicas en base a data entregada del stream ALeRCE-ZTF. 

Este proyecto se separa en dos jupyter notebooks para poder optimizar los procesos de ejecución de los algoritmos y no irrumpir en la data obtenida en cada una de las funciones correspondientes de los notebooks. Ambos notebooks se encuentran en el presente github y su orden de ejecutamiento corresponde al siguiente:

* 1) Curvas de luz y extracción de características
* 2) Reducción de dimensiones

A continuación se entregan los pasos a seguir para cada uno de los códigos correspondientes:

## Curvas de luz y extracción de características

Este jupyter notebook se divide en 5 secciones las cuales corresponden a las siguientes:

### 1) Librerías a importar para la experiencia

Dentro de esta sección se importan todas las librerias a utilizar para completar la experiencia. Una vez que se complete la instalación para las librerías **TurboFATS** y **lc_clssifier** favor de reiniciar el entorno de ejecución para poder importar las funciones que se encuentran en el bloque posterior.

### 2) Cargar la data a utilizar

Para poder desarrollar esta sección se tienen que cargar los datos iniciales entregados. El archivo correspondiente a **labels** se encuentra adjunto dentro de este github *(Dataframe -> datacurvasdeluz -> dataoriginal)*, sin embargo, el archivo correspondiente a **alert_detections** posee una gran cantidad de data por lo que no se pudo agregar de manera exitosa en este github sin que corrumpiera con los otros archivos, se pide porfavor crear una copia de este archivo dentro de su drive personal a partir del siguiente [Google Drive](https://drive.google.com/drive/folders/1EX7qSca6i-R8HOZMSushjxiW3YoPQ9Nw?usp=sharing) para poder trabajar de manera correcta con el archivo (el archivo se encuentra dentro de DataFrames).

### 3) Obtención de estrellas periódicas

Debido a que el proyecto corresponde específicamente a estrellas periódicas, se procede eliminando todas las estrellas que no correspondan de la data de **labels** creando una función auxiliar que recorra la data de labels y elimine aquellas estrellas no necesarias. Correr este bloque en su totalidad. Todas las estrellas periódicas quedan guardadas en la variable **labels**.

### 4) Sampling de estrellas y Curvas de Luz
Para trabajar de manera eficiente se obtuvieron **DataFrames** para cada una de las clases de estrellas a partir de las función **single_class**, dentro de este se pueden verificar las líneas de código comentadas para obtener cada una de clase. Para obtener los **DataFrame** de cada una de las clases porfavor descomentar la línea correspondiente a la clase que se desea recuperar. Debido a que al ejecutar este código se esta alterando el **DataFrame** de la sección anterior, si se quiere obtener una clase diferente favor comentar nuevamente la línea no correspondiente, descomentar la línea de la clase deseada y  ejecutar nuevamente los bloques correspondiente a la sección 2 y 3. Este proceso tiene un tiempo de ejecución de entre 3 y 5 minutos.

Para facilitar el desarrollo de los experimentos se guardaron cada uno de los **DataFrame** correspondientes a cada una de las clases en variables, favor de subir estos documentos en su copia de Drive personal para ejecutar. Estos **DataFrames** estan adjuntos en el github *(Dataframe -> datacurvasdeluz -> data separada en clases)*.

Para obtener las curvas de luz correspondientes se debe realizar un sampling para cada una de las clases de estrellas previamente, estas se guardan en la variable **oid_sample**. Para obtener el sample correspondiente a cada una de clases porfavor descomentar las líneas de codigo correspondiente a la clase con la que desee trabajar. Para obtener la curva de luz ejecute el código con la función **light_curve** con el **oid_sample** de su interés y la data de **alert_detections**. Estos resultados de curva de luz se guardan en la variable **df**.

## 5) Extracción de características

Para obtener finalmente las características de cada uno de los samples de las estrellas se debe realizar un preprocesamiento para la asignación de las bandas de luz r y g. Ejecutar el código correspondiente a **preprocessing** con su variable **df** obtenido en la sección anterior. El restultado de este proceso se guarda en la variable **df_prep**

Como paso final, ejecutar el código con la función **features** con su variable **df_prep**. Este proceso tiene un tiempo de ejecución de entre 8 y 10 minutos. Se pueden guardar los datos obtenidos con el bloque adjuntado al final, favor de descomentar en caso de que se requiera analizar.

Se da a fin la ejecución del primer jupyter notebook.

## Reducción de Dimensiones

### 1) Librerías a importar para la experiencia
Dentro de esta sección se importan todas las librerias a utilizar para completar la experiencia. Porfavor instalar las librerías en caso de que no las posea.

