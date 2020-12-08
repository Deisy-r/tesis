---
layout: post
title:  "Método de Bisección"
date:   2020-09-10 18:51:43 -0400
categories: senluv
tag: 1
---

*Método de Bisección*

![biseccion](/assets/images/biseccion.png)

Se considera un intervalo cerrado {% katex %}[a,b]{% endkatex %}, donde la función {% katex %}f(x){% endkatex %} cambia de signo, es decir, la imagen {% katex %}f(a).f(b)<0{% endkatex %}. El método consiste en ir dividiendo el intervalo *{% katex %}[a,b]{% endkatex %} por la mitad de la siguiente forma: 

- Se toma el punto medio:

{% katex %}\frac{a+b}{2}{% endkatex %}   si  {% katex %}f\frac {a+b}{2}=0{% endkatex %}  ya hemos encontrado la raíz 
{% katex %}x=\frac {a+b}{2}{% endkatex %}. 

En caso contrario, si  {% katex %}f(\frac {a+b}{2}).f(b)<0{% endkatex %} entonces hacemos {% katex %}a_1=\frac {a+b}{2}{% endkatex %} y volvemos a subdividir el nuevo intervalo {% katex %}[a,b]{% endkatex %}. 

Si, por el contrario,  {% katex %}f(a).f(\frac {a+b}{2})<0{% endkatex %}. Entonces hacemos {% katex %}b_1=\frac {a+b}{2}{% endkatex %} y volvemos a empezar las subdivisiones del intervalo {% katex %}[a,b]{% endkatex %} van aproximando la raíz. 

*NOTA: Cuando el punto medio no es raíz se debe verificar en que sub intervalo es raíz. Para determinarlo se puede elegir cualquiera de los dos sub intervalos generados por el punto medio y realiza sobre cualquier verificación. En caso de que no haya raíz en el automáticamente, se encontrara en el otro sub intervalo.*

**Teorema**

Sea {% katex %}f \epsilon C[a,b]{% endkatex %} supongamos que {% katex %}f(a).f(b)<0{% endkatex %} el procedimiento de bisección del algoritmo genera una sucesión {% katex %}{P_n}{% endkatex %} que aproxima a {% katex %}p{% endkatex %} con la propiedad {% katex %}|p_n-p|\leq\frac {b-a}{2^n}, n\geq1{% endkatex %}.

*Ejemplo:* 
Determine aproximadamente cuantas iteraciones son necesarias para resolver {% katex %}f(x)=x^3+4x^2-10{% endkatex %} con una precisión {% katex %}\varepsilon=10^{-5}{% endkatex %}  con {% katex %}[1,2]{% endkatex %}

![5](/assets/images/5.png)

.

.

.

_____________________________

**Iteración de Punto Fijo**


Consideremos una función {% katex %}g{% endkatex %} de la forma {% katex %}g(x)=x{% endkatex %} a una solución de esta ecuación se llama un punto fijo de la función {% katex %}g{% endkatex %}. 

Si para cualquier {% katex %}g{% endkatex %} dada se puede encontrar un punto fijo entonces cada problema de búsqueda de raíces podrá también ser resuelto. 


Por ejemplo, el problema de búsqueda de raíces {% katex %}f(x):= 0 {% endkatex %} tiene soluciones que corresponden precisamente a los puntos fijos {% katex %}g(x)=x-f(x){% endkatex %}.


*Ejemplo:* 

Sea {% katex %}g(x)=\frac {x^2-1}{3}{% endkatex %} {% katex %}[-1,1]{% endkatex %}

{% katex display %}x=0, g(0)=-\frac {1}{3} {% endkatex %}el máximo absoluto de {% katex %}g{% endkatex %} es {% katex %}x=\pm1{% endkatex %}
{% katex display %}g(\pm1)=0; g {% endkatex %} es continua
{% katex display %}|g'(x)|=|\frac{2}{3}x|=\frac{2}{3}|x|\leq k <1 {% endkatex %}

En este ejemplo el único punto fijo {% katex %}p{% endkatex %} en el intervalo {% katex %}[-1,1]{% endkatex %} puede determinarse exactamente {% katex %}p=g(p)=\frac{p^2-1}{3} {% endkatex %}, entonces 
{% katex display %}3p =p^2-1{% endkatex %}, donde {% katex %}p^2-3 p-1=0{% endkatex %}, {% katex %}p= \frac{3+\sqrt{13}}{2}{% endkatex %}

Notese  que {% katex %}g{% endkatex %} también tiene un único punto fijo {% katex %}p{% endkatex %} en {% katex %}p= \frac{3+\sqrt{13}}{2}{% endkatex %} en el intervalo {% katex %}[3,4]{% endkatex %}.


**Nota:** Para aproximar el punto fijo de una función {% katex %}g{% endkatex %}, escojamos una aproximación inicial {% katex %}p_0{% endkatex %} y generamos la sucesión {% katex %}{[p_n]}^\infty_n{% endkatex %} donde {% katex %}n=0{% endkatex %}. Tomando {% katex %}P_n=g(Pn-1), n\geq1{% endkatex %}.


Si la sucesión converge a {% katex %}p{% endkatex %} y {% katex %}g{% endkatex %} es continua, entonces {% katex %}P=\lim_{n \to \infty}p_n=\lim_{n \to \infty}{% endkatex %} {% katex %}(g(p_n-1))=g(\lim_{n \to \infty}{% endkatex %} {% katex %}P_n-1)=g(p){% endkatex %} y se obtiene una solución {% katex %}x=g(x){% endkatex %}. Esta técnica se llama **Técnica Iterativa del Punto Fijo**

