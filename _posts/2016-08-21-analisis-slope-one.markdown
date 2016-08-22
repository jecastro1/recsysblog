---
layout: post
title: "Análisis de: Slope One predictors for online rating-based collaborative filtering"
date: 2016-08-21 20:00 -0300
categories: any
---

En el paper **Slope One predictors for online rating-based collaborative filtering**, se propone que un sistema recomendador con predictores de la forma $$ f(x) = x + b $$ puede ser competitivo. Se compara principalmente con esquemas basados en correlación de Pearson y otros más sencillos.

En mi opinión, éste es un trabajo sencillo y conciso. Se colocan cinco propiedades deseables en un esquema de recomendación, y muestran que la propuesta de *slope one* cumple con ellas.

> Our goal in this paper is not to compare the accuracy of a wide range of CF algorithms but rather to demonstrate that the Slope One schemes simultaneously fulfill all five goals

Se podría tomar esta afirmación como **demasiado conveniente**, desde el punto de vista que acota bastante el trabajo. Sin embargo, lo presentado se puede entender en el contexto en que ya se veía difícil hacer una valuación *on the fly* con muchos usuarios e ítems.

Respecto a los esquemas que proponen tipo *slope one*, es adecuada la progresión entre ellos. Las mejoras sucesivas entre cada uno de ellos tienen sentido. Destaco la obervación al desarrollar el *Bi-polar slope one*, que indica que la distribución de los *ratings* no es uniforme.

Sin embargo, no se explica adecuadamente qué ocurre cuando el usuario activo tiene muy pocos ratings, a pesar de que uno de los aspectos que ellos buscaban con *slope one* es *"Expect little from first visitors: a user with few ratings should receive valid recommendations"*.

Por último, no se muestran más métricas que el **MAE** que muestren, por ejemplo, el *coverage* de cada esquema de recomendación testeado. Tampoco se aclara si los datasets se tomaron como venían, o si se tomó una muestra.

### Referencias

- Lemire, D., & Maclachlan, A. (2005, April). Slope One Predictors for Online Rating-Based Collaborative Filtering. In SDM (Vol. 5, pp. 1-5).
