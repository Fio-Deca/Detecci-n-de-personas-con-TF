# Detección-de-personas-con-TF

Descripción:En este projecto se creara una IA con deep learning para detectar personas utilizando una segmentación de imagenes de tipo instancias que se dividirá en 3 partes:

1- Distribución del dataset

2- Etiquetación 

3-Convertir .json a TFrecord

4- Entrenamiento de la red neuronal

Dataset utilizado: https://www.kaggle.com/datasets/constantinwerner/human-detection-dataset

Distribucion-dataset.py: El primer paso de este projecto será separar el  dataset en 70% para entrenar y el 30% para hacer el test

El siguente paso sera etiquetar las imagenes para ello iremos al siguiente link https://platform.linkedai.co/ el cual es una página web en la cual nos lo permitirá, en este caso primero etiquetaremos las imagenes de entreno y después las de test que estaran en projecto distintos.

![image](https://user-images.githubusercontent.com/57341284/167683732-90947df8-189a-4cc1-b224-d6f719260456.png)

Una vez etiquetadas todas las imagenes exportaremos las etiquetas (labels) en un .json 

json_tfrecords_test.py:este archivo nos permitira convertir el archivo que contenia las etiquetas en el Deteccion de personas - TEST.json  a un tfrecords para después poder entrenarlo con nuestro modelo
json_tfrecords_train.py:este archivo nos permitira convertir el archivo que contenia las etiquetas en el Deteccion de Personas - TRAIN.JSON  a un tfrecords para después poder entrenarlo con nuestro modelo
