---
layout: post
title:  "Polinomio Interpolante de Lagrange"
date:   2020-09-10 18:51:43 -0400
categories: interpolacion
tag: 2
---

##Polinomio Interpolante de Lagrange*

![lagrange](/assets/images/lagrange.png)

En análisis numérico el polinomio de Lagrange, interpola un conjunto de puntos dados en forma de Lagrange.

La reformulación del polinomio de Newton que evita el calculo por diferencias divididas es la siguiente: 
{% katex display %}f_n(x)=\sum^n_{i=0}L_i(x)f(x_i){% endkatex %} 
donde {% katex %}L_i(x)=\pi^n_{i=0,j\neq i}\frac{x-x_j}{x_i-x_j}{% endkatex %}.

**Teorema**
Si {% katex %}x_0,x_1,...,x_n{% endkatex %} son distintos en el intervalo {% katex %}[a,b]{% endkatex %} y si  {% katex %}f\in C^{n+1}[a,b]{% endkatex %} entonces para cada {% katex %}x\in[a,b]{% endkatex %} existe un número {% katex %}\xi(x){% endkatex %} en {% katex %}(a,b){% endkatex %} tal que {% katex %}f(x)=p(x)+\frac{f^{n+1}(\xi(x))}{(n+1)!}(x-x_0)(x-x_1)...(x-x_n){% endkatex %}

Donde {% katex %}P{% endkatex %} es el polinomio interpolante dado el siguiente: 

${% katex display %}p(x)=f(x_0)L_{n,0}(x)+...+f(x_n)L_{n,n}(x)={% endkatex %}

${% katex display %}\sum^n_{k=0}f(x_k)L_{n,k(x)}{% endkatex %}
