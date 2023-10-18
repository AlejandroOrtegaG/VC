# Práctica 2. Funciones básicas de OpenCV

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
Una encontrada la imagen que cumple con las características especificadas, usamos "HoughCircles" para localizar todos los círculos que se encuentran en la imagen, mediante un ajuste de los parámetros conseguimos detectar las 2 monedas que se encuentran solpadas, además del resto.
Una vez hecho esto, se pintan los cŕculos en la imagen, y tras pintarlos procedemos a redimensionar la imagen para que quepa en pantalla cuando se muestra, y por último definimos nuestro método(al cuál se le llamará cuando se detecte que se hace clic), dentro del cual se detecta donde se ha hecho clic, y mediante algunos cálculos, se establece si el clic ha sido dentro de una moneda de tamaño similar a la que estamos buscando. Para terminar, lo que se busca es si la moneda en la que estamos, tiene el color que necesitamos. Y tras esto, podemos determinar si se ha hecho clic en una moneda de un euro.

## Fragmentos, pellets y alquitrán
