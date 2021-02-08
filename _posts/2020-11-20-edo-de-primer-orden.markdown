---
layout: post
title:  "EDO de Primer Orden"
date:   2020-11-20 18:51:43 -0400
categories: edo
tag: 2
---



	Una ecuación diferencial de primer orden con el valor inicial se expresa de la siguiente forma: 

{% katex display %}
  [L]=\frac{d_y}{d_t}=f(t,y)y(t_0)=y_0
{% endkatex %}

Donde {% katex %}y(t_0)=y_0{% endkatex %} es la condición inicial. 

**Entre los tipos de ecuaciones diferenciales de primer orden se encuentran:**


 - **Ecuación de variables separables:** son de la forma  {% katex %}\frac{d_y}{d_t}=(t,y){% endkatex %} esta se puede expresar en la forma {% katex %}g(y)d_y=h(t)d_t{% endkatex %} en donde se procede integrando ambos miembros de la ecuación {% katex %}\int g(y)d_y= \int h(t)d_t{% endkatex %}, se supone que las funciones {% katex %}g{% endkatex %} y {% katex %}h{% endkatex %} son continuas. 

 
 - **Ecuación exacta:** es de la forma {% katex %}M(x,y)d_x+N(x,y)d_y=0{% endkatex %}, se dice exacta si existe una función {% katex %}F{% endkatex %} que cumpla {% katex %}\frac{\partial F }{\partial x}(x,y)=M{% endkatex %}  y {% katex %}\frac{\partial F }{\partial y}(x,y)=N{% endkatex %} . Su solución es entonces {% katex %}F(x,y)=C{% endkatex %} .

 
 - **EDO de primer orden y homogénea:** es la siguiente {% katex %}y'=f(x,y){% endkatex %} , con {% katex %}f(t_x,t_y)=t_f(x,y),\forall t \neq 0{% endkatex %} , para resolver se usa la sustitución {% katex %}y=xv{% endkatex %}, siendo {% katex %}v=v(x){% endkatex %}, una función desconocida, sin embargo, la palabra *“homogénea”* asume otro significado, dentro del estudio de las ecuaciones diferenciales ordinarias, fuera de este contexto.


 - **Ecuación lineal:** es líneas si presenta la forma {% katex %}y+P(x)y=Q(x){% endkatex %}, y que tiene por solución {% katex %}y(x)=e^{-\int P(x)d_x}(C+\int Q(x)e^{-\int P(x)d_x}d_x{% endkatex %} , es una ecuación diferencial de Bernoulli, con {% katex %}n=0{% endkatex %}. 

 
 - **Ecuación de Bernoulli:** es una generalización de la ecuación diferencial lineal, formulada por Jakob Bernoulli y resuelta por su hermano Johann Bernoulli, presenta la forma {% katex %}y+P(x)y=Q(x)y^n{% endkatex %}, en la cual si se le hace la sustitución {% katex %}z=y^{1-n}{% endkatex %}, la ecuación se transforma en una ecuación lineal con {% katex %}z{% endkatex %} como variable dependiente, resolviéndose de manera análoga. 

 
 - **Ecuación de Riccati:** esta ecuación diferencial introducida por Jacopo Francesco Riccati presenta la estructura {% katex %}y'(x)+P(x)y^2+Q(x)y+R(x)=0{% endkatex %}, para resolverla se debe hacer la sustitución {% katex %}y=y_P+\frac{1}{z}{% endkatex %}, donde {% katex %}y_P{% endkatex %} es una solución particular cualquiera de la ecuación.


 - **Ecuación de Lagrange:** presenta la forma {% katex %}y=g(y')x+f(y'){% endkatex %}, resolviéndose con la sustitución {% katex %}y=p{% endkatex %}, diferenciando y sustituyendo {% katex %}d_y{% endkatex %} por {% katex %}p d_x{% endkatex %}, se convierte a otra considerada en {% katex %}x{% endkatex %} como función de {% katex %}p{% endkatex %}, es lineal. 

 
 - **Ecuación de Clairaut:** llamada así en honor a Alexis-Claude Clairaut, tiene la forma {% katex %}y=xy'+f(y'){% endkatex %}, esta ecuación es una forma particular de la ecuación de Lagrange, con {% katex %}g(y')=y'{% endkatex %} , por lo cual, su resolución es análoga a la anterior. 

