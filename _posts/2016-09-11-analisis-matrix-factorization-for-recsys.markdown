---
layout: post
title: "Análisis de Matrix factorization techniques for recommender systems"
date: 2016-09-11 23:30 -0300
categories: any
---

El artículo **Matrix factorization techniques for recommender systems** apareció en la revista del IEEE. Trata sobre diferentes métodos de factorización matricial para recomendar ítems, pero al final se concentran en los aportes que hicieron los propios autores al área en el Netflix Prize.

En general el artículo es muy claro y didáctico, muestra bien los aportes que hay hasta ese entonces y las innovaciones hechas con el motivo del Netflix Prize.

## Detalles

Tal y como otros artículos antes del 2010, no hay análisis de complejidad computacional ni espacial de los algoritmos. Parece que si: estos algoritmos escalan mejor, pero queda al lector la labor de reproducir estos resultados, **lo que muchas veces no funciona**. Lo bueno es que ya se está notando la importancia de este aspecto.

Otro aspecto que me llamó la atención fue la mención a Simon Funk, quién utilizó gradiente estocástico para poder aprender los vectores $$p_{u}$$ y $$q_{i}$$. La explicación es clara, sin embargo, no se dice nada respecto a las condiciones de detención de tal algoritmo. Lo que se suele hacer es establecer un número determinado de épocas o esperar a que el error baje de cierto umbral, parámetros que uno quisiera conocer. Lo más triste de todo es que [la fuente citada](http://sifter.org/~simon/journal/20061211.html), del mismo Funk, tampoco dice algo al respecto.

Por último, no hay detalles de las implementaciones de Matrix factorization que usaron los autores con el dataset de Netflix. En concreto apunto a los algoritmos con dinámicas temporales, pues no hay ninguna mención a cómo tratan **exactamente** el tiempo.

# Referencias

- Koren, Y., Bell, R., & Volinsky, C. (2009). Matrix factorization techniques for recommender systems. Computer IEEE Magazine, 42(8), 30-37.
