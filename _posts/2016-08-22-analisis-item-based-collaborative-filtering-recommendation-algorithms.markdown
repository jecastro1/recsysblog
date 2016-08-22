---
layout: post
title: "Análisis: Item-based Collaborative Filtering Recommendation Algorithms"
date: 2016-08-22 01:22 -0300
categories: any
---

El último paper de esta semana es **Item-based Collaborative Filtering Recommendation Algorithms**. Lo principal de este trabajo es que se propone mirar primero los ítems similares al que queremos *rankear*, contrario al filtrado *user-based*. En general es un buen trabajo con un desarrollo claro.

Este *approach* se basa en el supuesto de que las relaciones entre ítems son relativamente estables en comparación con las relaciones entre usuario. Esto puede ser considerado razonable, pero olvida que en ciertos dominios podría ser importante considerar un efecto de *aging*.

## Cálculo de similaridad entre ítems

Al mostrar la valuación basada en el coseno entre los vectores $$ \vec{i} $$ y $$ \vec{j} $$, donde $$ i_{k} $$ corresponde al *rating* del usuario $$ k $$ sobre el ítem $$ i $$, falta mencionar que este método no funciona para escalas que contengan al 0. De hecho, reemplazar por 0 todas las valuaciones no hechas es lo mismo que no considerar a los usuarios que no hayan evaluado ambos ítems $$ i $$ y $$ j$$.

Por otra parte, habría sido de utilidad mostrar al lector el siguiente resultado:

$$

\cos(\vec{i}, \vec{j}) = \frac{\sum_{u \in U} R_{u, i} \cdot R_{u, j} }{\sqrt{\sum_{u \in U} R_{u, i}^2} \cdot \sqrt{\sum_{u \in U} R_{u, j}^2}}

$$

## Cálculo de la predicción

Al mostrar la suma con pesos, aparece la noción de "todos los ítems similares". Al parecer estos ítems similares de los que se habla, son los $$ k $$ más parecidos, que ellos mismos nombran como *model size*. Me parece que, si bien la suposición que acabo de hacer es razonable, debería aclararse en el mismo paper.

## Experimentación

Me hubiese gustado una mejor fundamentación de los resultados de los *benchmarks* de rendimiento. Quizás soy solo yo, pero un análisis un poco más profundo respecto a la complejidad de los cómputos podría haber explicado, por ejemplo, por qué para el mismo *model size* el impacto de train/test es mayor de $$ 0.3 $$ a $$ 0.5 $$ que de $$ 0.5 $$ a $$ 0.8 $$.

Otra cosa que no se puede dimensionar con un *benchmark* como el del paper, es qué tan potente era el equipo que usaron. Yo tuve mi primer computador el año 2003 y tenía 128 MB de RAM, y el computador del artículo es del 2001 y tenía ya 2 GB de RAM. Quizás los resultados no son tan buenos para la época, o quizás si.

Por último, decir que *It can be observed from the charts that the basic item-item algorithm out performs the user based algorithm at all values of $$x$$* es **arriesgado**. Esto porque no hay una metodología para decir que esa diferencia es realmente algo significativo y no una (afortunada) coincidencia. Ok, es fácil ver que el algoritmo *item-item* rinde tan bien como el *user based*, pero no más que eso.

# Referencias

- Sarwar, B., Karypis, G., Konstan, J., & Riedl, J. (2001, April). Item-based collaborative filtering recommendation algorithms. In Proceedings of the 10th international conference on World Wide Web (pp. 285-295). ACM.
