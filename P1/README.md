# Práctica 1 Visión por Computador

Esta práctica consistía en diferentes ejercicios relacionados con imágenes, tanto edición como detección dentro de las mismas. Para ello se ha utilizado Python como tecnología, y las librerías: OpenCV, Matplotlib y numpy.

## Participantes

[![GitHub](https://img.shields.io/badge/Alejandro-Ortega_González-blue)](https://github.com/AlejandroOrtegaG)
[![GitHub](https://img.shields.io/badge/Joaquín-Villamonte_Pereira-purple)](https://github.com/AlejandroOrtegaG)

## Índice

[Tablero de ajedrez](#tablero-de-ajedrez)

[Imagen estilo Mondrian](#imagen-estilo-mondrian)

[Imagen estilo Mondrian con OpenCV](#imagen-estilo-mondrian-con-opencv)

[Modificación de un plano](#modificación-de-un-plano)

[Círculos en las zonas más clara y oscura](#círculos-en-las-zonas-mas-clara-y-oscura)

[Propuesta Pop art](#propuesta-pop-art)

[Bibliografía](#bibliografía)

## Tablero de ajedrez
En este ejercicio, primero establecemos el ancho y al alto para nuestro tablero, esto se hace para que se puedan pintar los cuadrados más adecuadamente. Luego, se crea una imagen en blanco, con mapa de dolor en escala de grises, y por último, con un doble bucle se van pintando los cuadrados, de forma que queda con la textura de un tablero de ajedrez.
Al terminar, se reestablecen las dimensiones de la imagen para posteriores usos.

## Imagen estilo Mondrian
Para empezar, se crea una imagen en blanco sobre la que pintaremos. Para ello, hacemos uso de un bucle.En este bucle, pintaremos las líneas usando una seria de índices como valores. Tras terminar este bucle, empezaremos un segundo, en el cuál, haciendo uso de los mismos valores, pintaremos las zonas delimitadas por las líneas pintadas.
## Imagen estilo Mondrian con OpenCV
Se ha rehecho la tarea anterior, esta vez usando las funciones de pintado que nos ofrece OpenCV, en concreto, las funciones de línea y rectángulo
## Modificación de un plano
Para este apartado utilizamos la imagen del logo de la ULPGC. Hemos dividido en dos los valores de rojo de la imagen entera.
## Círculos-en-las-zonas-mas-clara y oscura
En este apartado usaremos la entrada de la cámara de nuevo. Para cumplir el objetivo de encontrar las zonas más clara y la más oscura de la entrada, se ha hecho otro doble bucle, pero en vez de ir de uno en uno, se aumenta de 8 en 8, así determinamos las zonas 8x8. Una vez determinadas, calculamos la media del valor RGB de todos los píxeles dentro de ésta, y en caso de ser mayor o menos que nuestros valores de umbral, los almacenamos, y así encontraremos, simultáneamente la zona más clara y la más oscura. Una vez hecho esto, solo falta almacenar ambas coordenadas y pintar un cículo en cada una.
## Propuesta-pop-art
Una vez más, usamos la entrada de vídeo. Hemos cogido el tercio vertical del medio del fotograma de la cámara, y hemos puesto los valores de cada plano en secciones diferentes del fotograma de salida, de manera que en la parte izquierda tenemos los valores de rojo, en la parte del medio tenemos los valores de azul, y en la derecha, los valores de verde.

## Bibliografía

[HTML Color Picker](https://www.w3schools.com/colors/colors_picker.asp)

[OpenCV VideoCapture](https://docs.opencv.org/3.4/d8/dfe/classcv_1_1VideoCapture.html)

[OpenCV WaitKey](https://www.geeksforgeeks.org/python-opencv-waitkey-function/)