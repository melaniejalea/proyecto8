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

Para poder desarrollar esta sección se tienen que cargar los datos iniciales entregados. El archivo correspondiente a **labels** se encuentra adjunto dentro de este github(Dataframe -> datacurvasdeluz -> dataoriginal), sin embargo, el archivo correspondiente a **alert_detections** posee una gran cantidad de data por lo que no se pudo agregar de manera exitosa en este github sin que corrumpiera con los otros archivos, se pide porfavor crear una copia de este archivo dentro de su drive personal a partir del siguiente [Google Drive](https://drive.google.com/drive/folders/1EX7qSca6i-R8HOZMSushjxiW3YoPQ9Nw?usp=sharing) para poder trabajar de manera correcta con el archivo (el archivo se encuentra dentro de DataFrames).

### 3) Obtención de estrellas periódicas

Debido a que el proyecto corresponde especificamente a estrellas periódicas, se procede eliminando todas las estrellas que no correspondan de la data de **labels** creando una función auxiliar que recorra la data de labels y dropee aquellas estrellas no necesarias. Correr este bloque en su totalidad.

### 4) Sampling de estrellas y Curvas de Luz
Para trabajar de manera eficiente se obtuvieron **DataFrames** para cada una de las clases de estrellas a partir de las función single_class, dentro de este se pueden verificar las líneas de código comentadas para obtener cada una de clase. Al ejecutar este código se esta alterando el **DataFrame** de la sección anterior, por lo que para obtener los **DataFrame** de cada una de las clases porfavor descomentar la línea correspondiente a la clase que se desea recuperar , si se quiere obtener una clase diferente favor de ejructar nuevamente el bloque correspondiente a la funcino pe upara ejercutar la sección anterior cada vez que se 
