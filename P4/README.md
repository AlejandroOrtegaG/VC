## Práctica 4. Detección de caras

Para esta práctica se daba total libertar para realizar una actividad usando los algoritmos de detección de cara proporcionados. Hemos usado el algoritmo "dlib 68", y con él, hemos hecho un filtro en que se vea que salen 2 rayos laser de los ojos del usuraio.

## Participantes

[![GitHub](https://img.shields.io/badge/Alejandro-Ortega_González-blue)](https://github.com/AlejandroOrtegaG)
[![GitHub](https://img.shields.io/badge/Joaquín-Villamonte_Pereira-purple)](https://github.com/jqvp)

# Filtro
Como se mencionó antes, para este filtro hemos hecho que al usuario le salgan unos rayos laser por los ojos, estos rayos laser se irán moviendo según donde mire el usuario, y además, si abre la boca, el rayo será mas grueso o más fino.
Esto se ha hecho aprovechando los puntos que nos proporciona el algoritmo dlib68, ya que se ha podido determinar hacia donde está mirando el usuario midiendo las distancias entre ellos o mirando el ángulo que forman.

![Presentación del filtro](laser.gif)