---
layout: post
title: "Análisis de Context-Aware Recommender Systems"
date: 2016-09-18 23:18 -0700
categories: any
---

El artículo **Context-Aware Recommender Systems** explora, según trabajos anteriores, los tipos de información contextual, los tipos de CARS según cómo incorporan esta información, dan casos de aplicación para contextos que no cambian con el tiempo y que son completamente observables, y luego concluyen con una serie de desafíos que vienen en el área.

Mi review tiene que ver con los paradigmas de uso de esta información de contexto. Los autores describen tres tipos y los analizan según cómo operan, sus ventajas y desventajas:

- Contextual *prefiltering* (de este quiero hablar)
- Contextual *postfiltering*
- Contextual *modeling*

Respecto al Contextual *prefiltering* señalan que una bondad es que con este método se pueden usar los recomendadores que ya existían, pues el contexto $$C$$ (de consulta) sirve para filtrar la información que servirá para evaluar qué recomendar. El contexto puede filtrar con dos enfoques:

1. Contexto exacto: los datos de entrada son sólo los que hacen match exacto con $$C$$
2. Contexto generalizado: un dato se considera si alguna generalización $$C_{d}^{g}$$ de su contexto $$C_{d}$$ coincide con la generalización $$C^{g}$$ de $$C$$.

Considero que una potencial desventaja (no tratada) de este modelo de *prefiltering* es el entrenamiento de los modelos que se usen después. Los conjuntos de datos de entrada pueden ser tantos como contextos posibles existan. Esto puede poner difícil dar respuestas rápidas, pues se deberá entrenar un modelo (que no era posible entrenar antes, a menos que tuvieran una técnica para adivinar la próxima consulta o que fueran realmente pocos contextos) y luego dar la respuesta, por cada consulta.

Otra dificultad es señalar contextos más generales. Un problema interesante sería revisar si la forma de generalizar influye o no, o experimentar con diferentes técnicas automáticas de generalización. El punto que quiero hacer es que cualquier cosa más difícil que un set de reglas decidido por los implementadores supone un desafío grande en varios aspectos, como elegir el contexto de menor tamaño que sea capaz de elegir una cantidad distinta de 0 de datos de entrada.

# Referencias

- Gediminas Adomavicius and Alexander Tuzhilin. 2008. Context-aware recommender systems. In Proceedings of the 2008 ACM conference on Recommender systems (RecSys ’08). ACM, New York, NY, USA, 335-336. http://www.aaai.org/ojs/index.php/aimagazine/article/view/2364
