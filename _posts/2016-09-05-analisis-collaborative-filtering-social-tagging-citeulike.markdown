---
layout: post
title: "Análisis de Collaborative filtering for social tagging systems: an experiment with CiteULike"
date: 2016-09-05 01:50 -0300
categories: any
---

Hoy, después de esta dura semana, analizaremos el paper **Collaborative filtering for social tagging systems: an experiment with CiteULike**.

## Overview

El artículo trata el problema del filtrado colaborativo en un contexto de **tags creados por el usuario**. Los autores señalan que el cambio más importante es que el contenido contribuído por los usuarios es más diverso en cuanto a naturaleza y calidad.


## Detalles

En la semana en que he tenido que lidiar con la poca escalabilidad de los algoritmos analizados antes, sigo viendo que los papers del área no incluyen un análisis básico de complejidad de tiempo y espacio de los nuevos algoritmos propuestos.

En ese sentido, este paper no es la excepción. No obstante, se le puede perdonar un poco porque los algoritmos presentados no son más que variantes pequeñas de otros que ya existían.

Es muy raro que se hayan elegido sólo 10 usuarios, aunque hayan sido de *carne y hueso*, para medir el rendimiento ¿No tenían más? Además, cada uno de ellos tenía a lo menos 50 artículos posteados, lo que podría tener el propósito de sacar métricas de rendimiento más confiables, pero a la vez olvidar los *problemas de siempre* de estos datasets.

Finalmente, a modo de opinión personal, no me gustó la forma en que desplegaron los gráficos de rendimiento de los algoritmos, pues la primera impresión depende mucho de cómo se ordenan los usuarios en el eje $$x$$.

# Referencias

- Parra, D., & Brusilovsky, P. (2009, October). Collaborative filtering for social tagging systems: an experiment with CiteULike. In Proceedings of the third ACM conference on Recommender systems (pp. 237-240). ACM.
