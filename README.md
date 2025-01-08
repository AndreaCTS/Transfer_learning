# Proyecto de transfer learning para la cirugía de extracción de vesícula

Se busca utilizar un modelo como Yolo V5 para poder hacer el reconocimiento objetos de las tres zonas de interés en la cirugía, que son :

-Surco de Rouvier
-Segmento IV
-Vesícula 

Estas zonas nos sirven para identificar cual es la región segura para cortar cierto tejido del cuerpo que permita extraer de zona segura la vesícula.

El proyecto llevó a cabo el siguiente proceso:
1. La preparación de las imágenes que se van a utilizar, se extraen los frame de varios videos de cirugías exitosas practicadas; Se obtienen en total más de 600 mil imágenes
2. Etiquetado de las zonas de interés, se usó la herramienta de VIA para etiquetar las imágenes en donde se puede evidenciar las zonas de interés en regiones cuadradas (Se etiquetan 1000 imágenes, para entrenamiento del modelo se usan 3000 divididas en tres categorías en total)
3. Se obtienen los csv de los cuadros delimitadores de cada una de las regiones presentes en las imágenes etiquetadas
4. Procesamiento de las imágenes , normalización de los datos de los cuadros delimitadores
5. Preparación de los datos en txt para cada imagen, apto para el modelo de Yolo V5
6. Division en train, test, validación
7. Entrenamiento del modelo
8. Evaluación de Métricas, los resultados se encuentran en la carpeta de **results**

## Resultados del proceso anterior:

Se muestran varias pruebas de imágenes, y algunas en las que el modelo identifica y señana de manera exitosa cada una de las regiones de interes mencionadas, mostrando también el porcentaje de confianza o certeza en esa predicción

![Captura de pantalla](https://raw.githubusercontent.com/AndreaCTS/imagenes/main/Screenshot%202025-01-08%20113725.png "Vista del proyecto")


