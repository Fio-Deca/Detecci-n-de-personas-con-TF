# Detección-de-personas-con-TF

Descripción: En este proyecto se creará una IA con deep learning para detectar personas utilizando una segmentación de imágenes de tipo instancias que se dividirá en 5 partes:

1- Distribución del dataset

2-Etiquetación 

3-Convertir .json a TFrecord

4-Entrenamiento de la red neuronal

5-Testeo de la red neuronal

Dataset utilizado: https://www.kaggle.com/datasets/constantinwerner/human-detection-dataset

El entorno utilizado para este proyecto ha sido Google Colab.

Distribucion-dataset.py: El primer paso de este projecto será separar el dataset en 70% para entrenar y el 30% para hacer el test.

El siguiente paso será etiquetar las imágenes, para ello iremos al siguiente link https://platform.linkedai.co/ el cual es una página web en la cual nos lo permitirá, en este caso primero etiquetaremos las imágenes de entreno y después las de test que estarán en proyecto distintos.

![image](https://user-images.githubusercontent.com/57341284/167683732-90947df8-189a-4cc1-b224-d6f719260456.png)

Una vez etiquetadas todas las imagenes exportaremos las etiquetas (labels) en un .json 

json_tfrecords_test.py:Este archivo nos permitirá convertir el archivo que contenía las etiquetas en el Deteccion de personas - TEST.json a un tfrecords para después poder entrenarlo con nuestro modelo

json_tfrecords_train.py:Este archivo nos permitirá convertir el archivo que contenía las etiquetas en el Deteccion de Personas - TRAIN.JSON a un tfrecords para después poder entrenarlo con nuestro modelo

entrenamiento_del_modelo.py: Aquí entrenaremos el modelo, en esta ocasión utilizaremos el modelo pre-entrenado SSD + MobileNetV2

Test.py: Nos permitirá usar el modelo que hemos creado a través de imágenes y videos

centroidtracker.py: Detectará objetos y los registrará

trackerobject.py: Identificará los objetos poniéndoles un ID
