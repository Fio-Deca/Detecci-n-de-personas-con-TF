# Detección-de-personas-con-TF :frowning_man:	

En este proyecto se creará una IA con deep learning para detectar personas utilizando una segmentación de imágenes de tipo instancias.

## Dataset Utilizado :books:	
https://www.kaggle.com/datasets/constantinwerner/human-detection-dataset

## Entorno de trabajo :test_tube:	
-Google Colab

## Partes del proyecto (código) :gear:	
 
### 1- Distribución del dataset :balance_scale:	

Distribucion-dataset.py: El primer paso de este projecto será separar el dataset en 70% para entrenar y el 30% para hacer el test.

### 2-Etiquetación :label:	

El siguiente paso será etiquetar las imágenes, para ello iremos al siguiente link https://platform.linkedai.co/ el cual es una página web en la cual nos lo permitirá, en este caso primero etiquetaremos las imágenes de entreno y después las de test que estarán en proyecto distintos.

![image](https://user-images.githubusercontent.com/57341284/167683732-90947df8-189a-4cc1-b224-d6f719260456.png)

Una vez etiquetadas todas las imagenes exportaremos las etiquetas (labels) en un .json 

### 3-Convertir .json a TFrecord :currency_exchange:	

json_tfrecords_test.py:Este archivo nos permitirá convertir el archivo que contenía las etiquetas en el Deteccion de personas - TEST.json a un tfrecords para después poder entrenarlo con nuestro modelo.

json_tfrecords_train.py:Este archivo nos permitirá convertir el archivo que contenía las etiquetas en el Deteccion de Personas - TRAIN.JSON a un tfrecords para después poder entrenarlo con nuestro modelo.

### 4-Entrenamiento de la red neuronal :weight_lifting_man:	

entrenamiento_del_modelo.py: Aquí entrenaremos el modelo, en esta ocasión utilizaremos el modelo pre-entrenado SSD + MobileNetV2.

### 5-Testeo de la red neuronal :1st_place_medal:	

Test.py: Nos permitirá usar el modelo que hemos creado a través de imágenes y videos.

### Otros archivos :notebook_with_decorative_cover:	 

centroidtracker.py: Detectará objetos y los registrará.

trackerobject.py: Identificará los objetos poniéndoles un ID.

# ¿Cómo usar la IA?

Para utilizar la IA lo que tendremos que hacer es importar el archivo test.py desde google colab, ahora tenemos que subir los archivos label_map.pbtxt ,el modelo_entrenado.zip y la imagen prueba1.png dentro del almacenamiento de sesión, simplemente ahora hay que correr el archivo.
