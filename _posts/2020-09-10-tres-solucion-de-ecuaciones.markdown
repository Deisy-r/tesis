---
layout: post
title:  "Solución de Ecuaciones no Lineales de una Variable: Método de Bisección"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---
**Solución de ecuaciones no Lineales de una variable**

*Método de Bisección*

Se considera un intervalo cerrado $[a,b]$, donde la función $f(x)$ cambia de signo, es decir, la imagen $f(a).f(b)<0$. El método consiste en ir dividiendo el intervalo *[a,b]* por la mitad de la siguiente forma: 

- Se toma el punto medio:
$\frac{a+b}{2}$   si   $f\frac {a+b}{2}=0$  ya hemos encontrado la raíz
$x=\frac {a+b}{2}$. en caso contrario, si  $f(\frac {a+b}{2}).f(b)<0$ entonces hacemos $a_1=\frac {a+b}{2}$ y volvemos a subdividir el nuevo intervalo $[a,b]$. Si, por el contrario, $f(a).f(\frac {a+b}{2})<0$. Entonces haceos $b_1=\frac {a+b}{2}$ y volvemos a empezar las subdivisiones del intervalo $[a,b]$ van aproximando la raíz. 

*NOTA: Cuando el punto medio no es raíz se debe verificar en que sub intervalo es raíz. Para determinarlo se puede elegir cualquiera de los dos sub intervalos generados por el punto medio y realiza sobre cualquier verificación. En caso de que no haya raíz en el automáticamente, se encontrara en el otro sub intervalo.*

**Teorema**
Sea $f \epsilon C[a,b]$ supongamos que $f(a).f(b)<0$ el procedimiento de bisección del algoritmo genera una sucesión ${P_n}$ que aproxima a $p$ con la propiedad $|p_n-p|\leq\frac {b-a}{2^n}, n\geq1$.

*Ejemplo:* 
Determine aproximadamente cuantas iteraciones son necesarias para resolver $f(x)=x^3+4x^2-10$ con una precisión  $\varepsilon=10$<sup>-5  con$[1,2]$

| n | $a_n$ | $b_n$ | $p_n$ | $f(p_n)$ |
|--|--|--|--|--|
| 1 | 1.0 | 2.0 |1.5  | 2.375 |
| 2 | 1.0 |1.5  | 1.25 | -1.79685 |
|  3| 1.25 | 1.5 |1.375  | 0.16211 |
|  4|  1.25| 1.375 |1.3125  | -0.8484 |
.
.
.
_____________________________
**Iteración de Punto Fijo**
Consideremos una función $g$ de la forma $g(x)=x$ a una solución de esta ecuación se llama un punto fijo de la función $g$. Si para cualquier $g$ dada se puede encontrar un punto fijo entonces cada problema de búsqueda de raíces podrá también ser resuelto. 
Por ejemplo, el problema de búsqueda de raíces $f(x):=0$ tiene soluciones que corresponden precisamente a los puntos fijos $g(x)=x-f(x)$.

*Ejemplo:* Sea $g(x)=\frac {x^2-1}{3}$ $[-1,1]$
$x=0, g(0)=-\frac {1}{3}$ el máximo absoluto de $g$ es $x=\pm1$
$g(\pm1)=0; g$ es continua
$|g'(x)|=|\frac{2}{3}x|=\frac{2}{3}|x|\leq k <1$

En este ejemplo el único punto fijo $p$ en el intervalo $[-1,1]$ puede determinarse exactamente $p=g(p)=\frac{p^2-1}{3}$, entonces 
$3p =p^2-1$, donde $p^2-3 p-1=0$, $p= \frac{3+\sqrt{13}}{2}$

Notese  que $g$ también tiene un único punto fijo $p$ en $p= \frac{3+\sqrt{13}}{2}$ en el intervalo $[3,4]$.

**Nota:** Para aproximar el punto fijo de una función $g$, escojamos una aproximación inicial $p_0$ y generamos la sucesión ${[p_n]}^\infty_n$ donde $n=0$. tomando $P_n=g(Pn-1), n\geq1$.
Si la sucesión converge a $p$ y $g$ es continua, entonces $P=\lim_{n \to \infty}$$p_n=\lim_{n \to \infty}$ $(g(p_n-1))=g(\lim_{n \to \infty}$ $P_n-1)=g(p)$ y se obtiene una solución $x=g(x)$. Esta técnica se llama **Técnica Iterativa del Punto Fijo**

