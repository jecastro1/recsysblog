---
layout: post
title: "Análisis: An algorithmic framework for performing collaborative filtering"
date: 2016-08-20 20:00 -0300
categories: any
---

Ahora es el turno de analizar el paper **An algorithmic framework for performing collaborative filtering**. En este paper se proponen mejoras a ciertos algoritmos de recomendación basados en filtrado colaborativo con métodos basados en vecinadades (o *neighborhood-based methods*). Las mejoras se concentran en ponderar mejor los factores en los que se basa la recomendación.

En este paper no me llamaron la atención demasiadas cosas como en el que analicé justo antes. Lo digo para bien, ya que en el anterior había encontrado cosas que **a mi juicio** ponían mucho ruido. Esta vez encontré un trabajo mejor desarrollado, más acotado en su definición y con resultados que se muestran con su respectivo proceso. Sin embargo, igualmente hay cosas que es válido poner en duda.

#### Metodología

Respecto a la metodología, plantean un *dataset* de ensueños. Un set de datos donde todos los usuarios tienen al menos 20 *ratings* establece un supuesto muy fuerte. Esto podría significar que los resultados de este paper no se pueden usar para cierto usuario hasta que éste alcance unos 20 *ratings*, lo que puede ser muy importante o no tanto en función del dominio.

 No me quedó claro si las métricas de *accuracy* y *decision-support* se calculaban por ítem o por usuario. Dado que que *coverage* se calcula sobre los ítems, he de pensar que ocurre lo mismo con estas métricas, pero creo que es necesario aclararlo.

#### Ponderando posibles vecinos

Me gusta el punto en que dan cuenta de que un vecino bien correlacionado pueda dar malas predicciones, debido a que esta buena correlación se obtiene de muy pocos ítems en común. Esto podría tener un efecto incluso mayor si se analizara en conjunto a otra parte del paper en que dicen que también hay películas más relevantes que otras. Lo malo es que tener en común 50 películas no es tan fácil (me imagino), habría que ver datos de plataformas actuales como Netflix.

#### Seleccionando vecinos

No queda claro a qué se debe que *best-n-neighbors* es mejor que *correlation-thresholding*, si es que para cierto $$ n $$ y cierto *threshold* ambas métricas pueden dar los mismos vecinos.

#### Conclusiones

Por último, no se ve de dónde se desprende la recomendación de usar correlación de Spearman o Pearson según el dominio de los puntajes de *ranking*.

### Referencias

- Herlocker, J. L., Konstan, J. A., Borchers, A., & Riedl, J. (1999, August). An algorithmic framework for performing collaborative filtering. In Proceedings of the 22nd annual international ACM SIGIR conference on Research and development in information retrieval (pp. 230-237).
