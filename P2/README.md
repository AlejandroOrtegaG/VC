# Práctica 2. Funciones básicas de OpenCV

## Participantes

[![GitHub](https://img.shields.io/badge/Alejandro-Ortega_González-blue)](https://github.com/AlejandroOrtegaG)
[![GitHub](https://img.shields.io/badge/Joaquín-Villamonte_Pereira-purple)](https://github.com/jqvp)

## Contenidos

[Análisis de Canny](#análisis-de-canny)

[Aplicación de Sobel sobre imagen](#aplicación-de-sobel-sobre-imagen)

[Análisis de Sobel y comparación](#análisis-de-sobel-y-comparación)

[Muestra de función sobre webcam](#muestra-de-función-sobre-webcam)

[Reinterpretación de procesamiento](#reinterpretación-de-procesamiento)

## Análisis de Canny
En este ejercicio se ha contado la cantidad de píxeles a 255 en las columnas y en las filas, hemos encontrado los máximos y hemos obtenido el número de columnas y filas con un valor mayor al 95% de cada valor máximo. Después se ha hecho una gráfica con el número de píxeles en blanco para filas y columnas, con una línea que marca el 95% del valor máximo.

## Aplicación de Sobel sobre imagen
Para este ejercicio hemos descargado una imagen `samoyedo.jpg`, a la que le hemos aplicado difuminado gaussiano, y a partir de este, hemos aplicado Sobel en los dos ejes y los hemos sumado. Por último, hemos mostrado el resultado tal cual, y también tras haberlo pasado a valores absolutos y escalado a 8 bits.

## Análisis de Sobel y comparación
En este apartado hemos aplicado las mismas técnicas que en el anterior, además de umbralizar la imagen, pero sobre la imagen del mandril, que se ha usado para el primer ejercicio, para comparar resultados. Además, hemos hecho el mismo análisis que en el primer ejercicio con esta imagen umbralizada. Se observa cómo este último paso permite un análisis de grano más fino, ya que se pueden incluir o excluir valores según la necesidad, en vez de solo tener disponible un conjunto de valores negros o blancos, como pasa con Canny.

## Muestra de función sobre webcam

## Reinterpretación de procesamiento
