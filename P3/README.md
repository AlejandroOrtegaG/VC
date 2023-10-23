# Práctica 3. Detección de formas

## Participantes

[![GitHub](https://img.shields.io/badge/Alejandro-Ortega_González-blue)](https://github.com/AlejandroOrtegaG)
[![GitHub](https://img.shields.io/badge/Joaquín-Villamonte_Pereira-purple)](https://github.com/jqvp)

## Contenidos

[Detección de monedas no solapadas](#detección-de-monedas-no-solapadas)

[Detección de monedas solapadas](#detección-de-monedas-solapadas)

[Fragmentos, pellets y alquitrán](#fragmentos-pellets-y-alquitrán)

## Detección de monedas no solapadas
Para este ejercicio se pide que, en al menos una imgagen en la que aparecen monedas no solapadas, se detecten y se visualicen los bordes de las mismas, dejando fuera los objetos que no corresponden con monedas. Esto se ha hecho haciendo uso de varios métodos para la detección de bordes como "findContours". Más adelante analizamos cada contorno que se ha detectado y mediante varios pasos de filtrado determinamos si se trata de un objeto que podemos categorizar como moneda o si lo descartamos, para finalmente mostrarlo en nuestra imagen final o no. Una vez decidido los bordes que debemos pintar, simplemente mostramos una cuenta que nos dice cuantas monedas se han detectado en la imagen.
Para facilitar la detección, hemos aplicado un umbralizado a la imagen para poder así descartar más fácilmente lo que no nos interesa y agilizar el proceso.

## Detección de monedas solapadas
En la segunda tarea se pide utilizar al menos una imagen en la que aparezcan monedas solapadas. En esta imagen debemos detectar una moneda de un euro mediante un clic, y tras esto, calcular la cantidad de dinero que hay en la imagen.
Una vez hecha la imagen que cumple con las características especificadas, usamos "HoughCircles" para localizar todos los círculos que se encuentran en la imagen, mediante un ajuste de los parámetros conseguimos detectar las 2 monedas que se encuentran solpadas, además del resto.
Una vez hecho esto, se pintan los círculos en la imagen, y tras pintarlos procedemos a redimensionar la imagen para que quepa en pantalla cuando se muestra, y por último definimos nuestra función de detección, dentro del cual se detecta en qué círculo se ha hecho clic, y se establecen unos grupos de círculos según su tamaño respecto a la referencia (un euro). Para terminar, en caso de hacer falta, se determina el color (plateado, dorado o bronce) para saber el tipo de moneda que es. Con esto podemos ordenar las monedas según el tamaño y el color, de manera que aunque los tamaños sean parecidos, podemos discernir entre una moneda de 5 céntimos o una de 10, y así sacar la cantidad total de dinero.

## Fragmentos, pellets y alquitrán
En este apartado se han importado tres imágenes, una para cada tipo de residuo. Estas imágenes se recortan, pasan a gris y umbralizan. Para cada imagen, se le ha aplicado una detección de contornos, y por cada contorno, se mira si su contenido es negro, mediante el aplicado de la máscara del contorno. Si lo es, lo más probable es que sea una partícula de alquitrán. En caso contrario, se compara el área del círculo que lo encapsula con el área del contorno. Si es suficientemente parecida, se clasifica como pellet. En caso contrario, se clasifica automáticamente como fragmento.
