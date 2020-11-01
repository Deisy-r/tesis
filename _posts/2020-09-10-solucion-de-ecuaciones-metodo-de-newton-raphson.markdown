---
layout: post
title:  "Método de Newton-Raphson"
date:   2020-09-10 18:51:43 -0400
categories: senluv
tag: 3
---
*Método de Newton Raphson*

Es uno de los métodos numéricos más conocidos y más poderosos para la búsqueda de la solución de {% katex %}f(x):=0{% endkatex %}.

Si el valor inicial para la raíz es {% katex %}x_n{% endkatex %} entonces se puede trazar una tangente desde el punto {% katex %}[x_i, f(x_i)]{% endkatex %} de la curva. Por lo común, el punto donde esta tangente cruza al *eje x* representa una aproximación mejorada de la raíz.


La siguiente fórmula:
{% katex display %}f'(x_i)=/frac{f(x_i)-0}{x_i-X_{i+1}}{% endkatex %}.

Se arregla para obtener:
{% katex display %}x_{i+1}=x_i/frac{f(x_i)}{f'(x_i)}{% endkatex %}
la cual se conoce como **fórmula de Newton-Raphson**
