---
layout: post
title:  "Interpolación y Diferencias Divididas"
date:   2020-09-10 18:51:43 -0400
categories: interpolacion
tag: 3
---

##DIFERENCIAS DIVIDIDAS

Supongamos que {% katex %}P_n{% endkatex %} es un polinomio de lagrange de grado {% katex %}n{% endkatex %} que coincide con la función {% katex %}f{% endkatex %} con los números distintos {% katex %}x_0,x_1,x_2,...,x_n{% endkatex %}. Se pueden derivar que {% katex %}p_n{% endkatex %} tiene la siguiente representación: 

{% katex display %}P_n(x)=a_0+a_1(x-x_0)+a_2(x-x_0)(x-x_1)+...+a_n(x-x_0)(x-x_1)...(x-x_{n-1}){% endkatex %}

Simultáneamente cuando {% katex %}P_n{% endkatex %} se evalúa en {% katex %}x_1{% endkatex %} los únicos términos distintos de cero en la evaluación {% katex %}P_n(x_1){% endkatex %}

{% katex display %}f(x_0)+a_2(x_1-x_0)\equiv P_n(x_1)=f(x_1){% endkatex %}

Así despejando las constantes
{% katex display %}a_1(x_1-x_0)=f(x_1)-f(x_0){% endkatex %}
{% katex display %}a_1=\frac {f(x_1)-f(x_0)}{x_1-x_0}{% endkatex %}

Así que introducimos lo que se conoce como *notación de diferencias divididas*

La diferencia dividida {% katex %}0{% endkatex %} *(cero)* de la función {% katex %}f{% endkatex %} con respecto a {% katex %}x_1{% endkatex %} se denota {% katex %}f[x_1]{% endkatex %}, es simplemente la evaluación de {% katex %}f{% endkatex %} en {% katex %}x_1{% endkatex %}.

Las diferencias divididas restantes se definen inductivamente, la primera diferencia dividida de {% katex %}f{% endkatex %} con respecto a {% katex %}x_i{% endkatex %} y {% katex %}x_{i+1}{% endkatex %}, se denota {% katex %}f[x_i,x_{i+1}]{% endkatex %}y esta definida por:
{% katex display %}\frac{f[x_{i+1}]-f[x_i]}{x_{i+1}-x_i}{% endkatex %}
