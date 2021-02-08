---
layout: post
title:  "Método de Newton-Raphson"
date:   2020-09-10 18:51:43 -0400
categories: senluv
tag: 3
---
*Método de Newton Raphson*

![NR](/assets/images/NR.png)

Es uno de los métodos numéricos más conocidos y más poderosos para la búsqueda de la solución de {% katex %}f(x):=0{% endkatex %}.

Si el valor inicial para la raíz es {% katex %}x_n{% endkatex %} entonces se puede trazar una tangente desde el punto {% katex %}[x_i, f(x_i)]{% endkatex %} de la curva. Por lo común, el punto donde esta tangente cruza al *eje x* representa una aproximación mejorada de la raíz.


La siguiente fórmula:
{% katex %}f'(x_i)= \frac{f(x_i)-0}{x_i-X_{i+1}}{% endkatex %}


Se arregla para obtener:

{% katex %}x_{i+1}=x_i \frac{f(x_i)}{f'(x_i)}{% endkatex %}


la cual se conoce como **fórmula de Newton-Raphson**

*Ejemplo:*
Aproxima la solución de {% katex %}e^x= \frac{1}{x}{% endkatex %} con {% katex %}6{% endkatex %}decimales exactos.

Representamos las curvas 
{% katex %}y=e^x{% endkatex %} y {% katex %}y= \frac{1}{x}{% endkatex %}

![ejm](/assets/images/ejm.png)

Está claro que hay una solución. Tomamos como valor inicial {% katex %}x_0=0.5{% endkatex %}.
Escribimos la ecuación en la forma {% katex %}f(x)=0{% endkatex %}, con 

{% katex display %}f(x)=e^x- \frac{1}{x}{% endkatex %}


Derivada {% katex %}f'(x)=e^x+ \frac{1}{x^2}{% endkatex %}

Método.

.
.
.
El resultado de las iteraciones y los errores estimados es {% katex %}x_0=0.5{% endkatex %}


{% katex display %}x_1=0.5- \frac{e^{0.5}-\frac{1}{0.5}}{e^{0.5}+\frac{1}{(0.5)^2}} =0.56218730, \mid e_1 \mid = \mid x_1-x_0 \mid= 0.0621873{% endkatex %} 


{% katex display %}x_2=0.56711982, \mid e_2 \mid = \mid x_2-x_1 \mid= 0.00493252, {% endkatex %} 



{% katex display %}x_3=0.56714329, \mid e_3 \mid = \mid x_3-x_2 \mid= 0.00002347, {% endkatex %}



{% katex display %}x_4=0.56714329, \mid e_4 \mid = 0 {% endkatex %}

El resultado es: 

{% katex display%}\alpha =0.567143{% endkatex %}



El valor de la raíz con 10 decimales es:

{% katex %}\alpha =0.5671432904{% endkatex %}
