---
layout: post
title: "Análisis de Recommender Systems: Sources of Knowledge and Evaluation Metrics"
date: 2016-08-29 01:50 -0300
categories: any
---

Lo de hoy no es exactamente un paper, sino que un capítulo de un libro. Se trata de **Recommender Systems: Sources of Knowledge and Evaluation Metrics**, cuyo objetivo es presentar las fuentes de donde se suelen extraer los datos, y las métricas más importantes para evaluar los sistemas recomendadores.

## Overview

El artículo **establece una clasificación de los sistemas recomendadores y posibles métricas para medir el rendimiento de ellos**. Me parece importante tener en mente que el objetivo de este trabajo no era publicar un hallazgo nuevo, sino que recopilar los más importantes del área en un conjunto de ideas consistente. En ese sentido, el objetivo se cumple muy bien y podría ser tomado como un primer **marco de referencia para quien se proponga entrar en el área**.

En este [blog](http://bickson.blogspot.cl/2012/10/the-10-recommender-system-metrics-you.html) hay un mail de uno de los autores de este capítulo de libro, que resume las métricas que aparecen ahí.

## Detalles

Me hubiese gustado un poco de mayor extensión respecto a los métodos para obtener *implicit feedback*, o haber aclarado que no existían más ideas o métodos al respecto.

También faltó una sección en que se hablara de test estadísticos para comparar recomendadores. No es raro encontrar papers en que se afirma que un recomendador es mejor que otro en resultados, sin probar que no fue sólo suerte.

Finalmente, al leer la sección de **"Sources for Knowledge for Web Recommendation"** me dio la sensación de encontrarme con una visión un poco antigua, sobre todo respecto a la información disponible del lado del servidor. Me imagino que en la actualidad la información registrada allí es más que un log de *requests*, pero que en el año de la cita (2005) **era lo que había**.

# Referencias

- Parra, D., & Sahebi, S. (2013). Recommender systems: Sources of knowledge and evaluation metrics. In Advanced Techniques in Web Intelligence-2 (pp. 149-175). Springer Berlin Heidelberg.
