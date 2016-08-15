---
layout: post
title: "Análisis de GroupLens: an open architecture for collaborative filtering of netnews"
date: 2016-08-14 22:05 -0300
categories: any
---

Un poco más tarde de lo que tenía presupuestado, voy analizar un paper bien antiguo (octubre de 1994). Se trata de **GroupLens: an open architecture for collaborative filtering of netnews**. En este paper se propone una arquitectura para recomendar artículos con la técnica de filtrado colaborativo.

#### Generalidades

En relación a los trabajos relacionados que se en el paper se habla de The Tapestry system, que parece ser muy similar a GroupLens. En mi opinión, los autores definen las diferencias de su trabajo con The Tapestry **excesivamente** en función de la arquitectura y muy poco en relación a cómo funcionan las recomendaciones.

Faltan muchos detalles cuando dicen que hicieron una prueba piloto, en la que determinaron que un grupo de siete personas no era suficiente para aprovechar el filtrado colaborativo. Por ejemplo: no da una hipótesis de por qué esto sucede, no muestra cómo hicieron esa prueba, ni da los criterios para decidir que el filtrado colaborativo no funciona.

>
We have investigated several techniques for correlating past behavior and using the resultant weights, based on reinforcement learning, multivariate regression, and pairwise correlation coefficients that minimize linear error or squared error.

Esta afirmación es completamente irrelevante, pues al leer el artículo no se muestra que hayan analizado todas estas posibilidades. De hecho, después se limitan a decir que *"It seems likely that better scoring mechanisms can be developed"*.

#### Coeficiente de correlación

{: .center}
![Correlation coefficient formula]({{ site.baseurl }}/assets/GroupLens-corr-equation.png)

Respecto a la forma de calcular este coeficiente, se dice que incluso los promedios de las evaluaciones son calculados sobre los ítems que tienen los usuarios $$K$$ y $$L$$. Me imagino que la idea de tomar el promedio de cada usuario es ver qué tal son evaluando, si es así entonces estarían cometiendo un error al no considerar todos sus ratings.

Además, no se indica qué hacer en caso de que uno de los usuarios sea nuevo.

#### Cálculo de puntajes

{: .center}
![Score formula]({{ site.baseurl }}/assets/GroupLens-score-equation.png)

Los autores señalan usar todos los usuarios para predecir el puntaje del usuario activo. No hay mayor análisis en las implicancias de actuar bajo la lógica de **si lo que le gusta a él no me gusta a mi, y a él no le gusta algo, entonces me gustará a mi**.

#### Separación por tópicos

Me pareció correcto considerar la separación del filtrado colaborativo por temas, bajo el supuesto de que no siempre que dos personas estén de acuerdo en artículos académicos podrían estarlo en artículos sobre chistes. Habría sido interesante mostrar qué tanto baja el nivel de las recomendaciones utilizando la misma matriz para todo, pero me imagino que lo dejaron para otro trabajo.

#### Implicancias

Por último, me parece acertado el análisis de cuando un grupo de usuarios reducido coloca ratings muy bajos a un artículo nuevo. Incluso agregaría que puede ser una posible fuente de sabotaje para que nadie vea ciertos artículos. Este es un problema que podría seguir siendo importante en la actualidad.


### Referencias

- Resnick, P., Iacovou, N., Suchak, M., Bergstrom, P., & Riedl, J. (1994, October). GroupLens: an open architecture for collaborative filtering of netnews. In Proceedings of the 1994 ACM conference on Computer supported cooperative work (pp. 175-186). ACM.
