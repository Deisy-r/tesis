---
layout: post
title:  "Integración Númerica"
date:   2020-09-10 18:51:43 -0400
categories: in
tag: 0
---


## Fórmula de Newton-Cotes

Nombradas así por *Isaac Newton* y *Roger Cotes*, en las cuales se evalúa la función en puntos equidistantes, para así hallar un valor aproximado de la integral. Cuanto más intervalos se divida la función más preciso será el resultado.

**Regla del Trapecio Simple**


La regla del trapecio es la primera regla cerrada del Newton-Cotes. 
Gráficamente:


![Regla De Los Trapecios](https://userscontent2.emaze.com/images/514d0b1f-1b44-412c-b275-a762667c3dc1/ecab57c3-f717-4c1f-8641-d700e8303044png)



Donde: {% katex %}p(x)=f(a)+\frac{f(b)-f(a)}{b-a}(x-a){% endkatex %} , {% katex %}f(x)=mx+b{% endkatex %}.

El área bajo esta linea recta es una aproximación del área bajo la curva entre los limites {% katex %}a{% endkatex %} y {% katex %}b{% endkatex %}.

{% katex display %}\int^b_af(x)d_x\approx\int^b_a(f(a)+\frac{f(b)-f(a)}{b-a}(x-a))d_x{% endkatex %}

{% katex display %}\approx[f(a)+\frac{f(b)-f(a)}{b-a}\frac{(x-a)^2}{2}]^b_a{% endkatex %}

{% katex display %}\approx(b-a)\frac{f(a)+f(b)}{2}{% endkatex %}


Una estimación al **error de truncamiento local** para una sola aplicación de la regla del trapecio es

{% katex display %}E_t=-\frac{1}{12}f''(\xi)(b-a)^3{% endkatex %}


Donde {% katex d%}\xi{% endkatex %} está en algun lugar en el intervalo de {% katex %}a{% endkatex %} a {% katex %}b{% endkatex %} 


**Regla del Trapecio Compuesto**


Una forma de mejorar la precisión de la regla del trapecio consiste en dividir el intervalo de integración de a a b en varios segmentos, y aplicar el método a cada uno de ellos. Las áreas de los segmentos se suman después para obtener la integral en todo el intervalo.


{% katex display %}I=(b-a)\frac{f(x_0)+2\sum^{n-1}_{i=1}f(x_i)+f(x_n)}{2n}{% endkatex %}

Para estimar el error aproximado
{% katex display %}E_a=\frac{(b-a)^3}{12n^2}f''{% endkatex %}
 


**Regla de Simpson** {% katex %}\frac{1}{3}{% endkatex %}


Resulta cuando un polinomio de interpolación de segundo grado se sustituye en la ecuación: 

{% katex display %}\int^b_af(x)d_x\approx \int^b_af_2(x)d_x{% endkatex %}

Expresandose

{% katex display %}I=(b-a)\frac{f(x_0)+4f(x_1)+f(x_2)}{6}{% endkatex %}

Donde {% katex %}a=x_0, b=x_2{% endkatex %} y {% katex %}x_1={% endkatex %} el punto a la mitad entre {% katex %}a {% endkatex %} y {% katex %} b{% endkatex %},que esta dado por {% katex %}\frac{(b-a)}{2}{% endkatex %}

La aplicación de esta regla tiene un error de truncamiento con 

{% katex display %}E_t=-\frac{(b-a)^5}{2880}f^{(4)}(\xi){% endkatex %}

Donde {% katex %}\xi{% endkatex %}está en algún lugar en el intervalo de {% katex %}a {% endkatex %} a {% katex %} b{% endkatex %}



**Regla de Simpson** {% katex %}\frac{1}{3}{% endkatex %} **de aplicación múltiple**


Así como en la regla del trapecio, la regla de Simpson se mejora al dividir el intervalo de integración en varios segmentos de un mismo tamaño
{% katex display %}I \cong (b-a) \frac{f(x_0)+4 \sum ^{(n-1)}_{i=1,3,5}f(x_i)+2 \sum ^{(n-2)}_{j=2,4,6}f(x_j)+f(x_n)}{3n}{% endkatex %}


Un **error estimado en la regla de Simpson de aplicación múltiple** se obtiene de la misma forma que en la regla del trapecio: sumando los errores individuales de los segmentos y sacando el promedio de la derivada para llegar a 

{% katex display %}E_a=-\frac{(b-a)^5}{180n^4}f^{(4)}{% endkatex %}

Donde {% katex %}f^{(4)}{% endkatex %} es el promedio de la cuarta derivada en el intervalo.



**Regla de Simpson** {% katex %}\frac{3}{8}{% endkatex %}

De manera similar a la obtención de la regla del trapecio y Simpson 1/3, es posible ajustar un polinomio de Lagrange de tercer grado a cuatro puntos e integrarlo:

{% katex display %}I \cong (b-a) \frac{f(x_0)+3f(x_1)+3f(x_2)+f(x_3)}{8}{% endkatex %}

Así los dos puntos interiores tienen pesos de tres octavos, mientras que los puntos extremos tienen un peso de un octavo. La regla de Simpson 3/8 tiene un error de:


{% katex display %}E_t=-\frac{(b-a)^5}{6480}f^{(4)}(\xi){% endkatex %}

