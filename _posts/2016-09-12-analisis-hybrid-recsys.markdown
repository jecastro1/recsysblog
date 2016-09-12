---
layout: post
title: "Análisis de Hybrid Recommender Systems: Survey and Experiments"
date: 2016-09-12 02:07 -0300
categories: any
---

El paper **Hybrid Recommender Systems: Survey and Experiments** propone una clasificación de los sistemas recomendadores híbridos, o sea, los que usan más de uno de los de base. Para esto ofrece un análisis de las ventajas y desventajas de cada sistema por separado.

La contribución más importante que deja el artículo es establecer qué tipos de sistemas híbridos están estudiados, cuales están por estudiar, y cuáles no tiene sentido estudiar. Esto sin duda dio origen a muchas más investigaciones, de hecho, [según Google Scholar](https://scholar.google.com/scholar?hl=es&q=Hybrid+Recommender+Systems%3A+Survey+and+Experiments&btnG=&lr=) hay más de 2900 citas a este trabajo, las que incluyen artículos recientes.

Además, se toma el híbrido de un User-CF con un Knowledge-Based, bajo el esquema de Cascada y se analiza un caso particular. Muestran que la combinación *vino bien*.

## Detalles

Considero que el artículo está bien hecho, para ser del año que es. Señala varias cosas que en otros no, como por ejemplo, niveles de significancia para decir que un algoritmo es mejor que otro, tamaño del dataset, cómo se obtuvo este, análisis respecto a un baseline, el número de vecinos del algoritmo User-CF (¡sólo uno!, ¿Por qué tan pocos?), entre otros.

No obstante, se podría pensar que la métrica de distancia que ellos llaman "heurística" está artificalmente armada. Si bien los supuestos ahí mostrados se ven razonables, considero que hace más difícil traspasar los resultados de este trabajo a otro de diferente dominio **y las cosas podrían ser muy distintas**.

Otra cosa a destacar es que la métrica se armó y explicó en el mismo paper. Quizás no sea la mejor métrica, pero potencialmente ayudó a generar investigación respecto a cómo medir los recomendadores híbridos.

# Referencias

- Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix factorization techniques for recommender systems. Computer IEEE Magazine, 42(8), 30-37.
