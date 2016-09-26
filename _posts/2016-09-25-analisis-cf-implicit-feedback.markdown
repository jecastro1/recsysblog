---
layout: post
title: "Análisis de Collaborative Filtering for Implicit Feedback Datasets"
date: 2016-09-26 02:00 -0800
categories: any
---

El artículo **Collaborative Filtering for Implicit Feedback Datasets** explora la posibilidad de utilizar implicit feedback con un *approach* de filtrado colaborativo. Trata los desafíos que tiene utilizar estos datos en vez de explicit feedback y propone:

1. Un modelo para extraer datos desde implicit feedback
2. Un algoritmo basado en factorización matricial
3. Una forma de explicar estas recomendaciones

El gran aporte de este trabajo es mostrar los desafíos que tiene utilizar implicit feedback, con el beneficio de obtener muchos más datos.

Una crítica que haría al trabajo es que los ajustes realizados al mapeo de los datos a $$(preference, confidence)$$ es muy *domain-dependant*. Sin embargo, **es muy razonable** pensar que un $$confidence$$ de forma logarítmica como el mostrado pueda funcionar igual de bien con otros datasets, pues no es tan intuitivo pensar que mi gusto por $$A$$ es el doble que por el de $$B$$ sólo porque $$A$$ lo he visto el doble de veces.

Otra cosa que me llamó la atención es el análisis de complejidad del algoritmo. Cosa positiva es que ya esté empezando a aparecer en los trabajos del área. Ahora, si bien se muestra que el tiempo es lineal en el tamaño del input, no se hace mayor reflexión respecto a que es cúbico respecto a la cantidad de factores latentes. No es tan grave, pues lo que más crece (y lo que más nos importa) es la cantidad de datos de entrada. Pero, tomando en consideración lo mucho que mejoran sus experimentos tomando 100 factores latentes en vez de 10, no es menor que hacer eso haya tardado 1000 veces más.


# Referencias

- Hu, Y., Koren, Y., & Volinsky, C. (2008, December). Collaborative filtering for implicit feedback datasets. In Data Mining, 2008. ICDM’08. Eighth IEEE International Conference on (pp. 263-272). IEEE.
