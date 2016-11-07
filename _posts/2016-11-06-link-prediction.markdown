---
layout: post
title: "Análisis de Link Prediction Problem for Social Networks"
date: 2016-11-06 22:00 -0300
categories: any
---

El artículo **Link Prediction Problem for Social Network** el problema de link prediction. Dado un grafo de una red social o similar, se quiere predecir qué links se formarán en el futuro. 

Se realizan experimentos con cinco datasets de papers y autores, donde la intención es predecir con los datos más antiguos qué autores colaborarán en el futuro. Se analizan varios métodos, desde *random*, pasando por métodos que cuentan los vecinos en común entre dos nodos, hasta métodos más sotisficados como *PageRank*.

La comparación es interesante y en general se concluye que es buena idea investigar sobre el tema, puesto que se demuestra que los resultados mejoran usando uno u otro approach. Además, la observación de que se debió ponderar mejor las interacciones recientes es acertada.

Sin embargo, los resultados no son concluyentes respecto a cuál de los métodos más sotisficados podría ser el mejor, de hecho en las figuras se muestran que sólo comparar los vecinos en común es mejor que varios métodos y comparable con otros más. También se revisa el problema de *small worlds* y que a veces se forma un link con nodos de distancia mayor que dos, pero de alguna manera siento que estos problemas se contradicen el uno con el otro (hasta cierto punto) y hace que la conclusión del paper sea menos limpia.

# Referencias

- David Liben-Nowell and Jon Kleinberg. 2007. The link-prediction problem for social networks. J. Am. Soc. Inf. Sci. Technol. 58, 7 (May 2007), 1019-1031.
