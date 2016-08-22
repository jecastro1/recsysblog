---
layout: post
title: "Análisis: How not to sort by Average Rating"
date: 2016-08-11 23:00 -0400
categories: any
---

En esta ocasión voy a analizar un [artículo del blog de Evan Miller](http://www.evanmiller.org/how-not-to-sort-by-average-rating.html), que muestra soluciones deficientes al problema de recomendación Top-N. Antes de seguir, es importante recalcar que el post es del año 2009.

El artículo muestra acertadamente dos ejemplos de implementaciones *naïve*. Si bien entrega un caso en que la implementación de Amazon podría funcionar bien, no hace lo mismo con la de Urban Dictionary, aunque se entiende que ésta sea "poco defendible".

Respecto a la solución que se propone, la explicación dada no profundiza demasiado respecto a las razones que hay para considerarla adecuada, ni tampoco habla más sobre qué ocurre cuando hay pocos datos.

Además, da la sensación de que se busca explicar una fórmula para programadores sin un *background* estadístico fuerte, pero que a la vez omite detalles importantes para un principiante. Por ejemplo: nunca explica qué es el parámetro α, qué significa en términos numéricos el que se admitan sólo calificaciones binarias, y además omite que la ecuación muestra una *lower bound* y una *upper bound* a la vez.

No obstante, rescato que el artículo es un muy buen recurso para quienes buscan una idea rápida sobre cómo hacer recomendaciones sin tener los conocimientos que se necesitan.

# Links

- [How not to sort by Average Rating - Evan Miller](http://www.evanmiller.org/how-not-to-sort-by-average-rating.html)
