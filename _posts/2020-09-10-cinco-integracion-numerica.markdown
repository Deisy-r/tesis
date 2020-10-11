---
layout: post
title:  "Integración Númerica"
date:   2020-09-10 18:51:43 -0400
categories: pagina
---
## INTEGRACIÓN NUMÉRICA
*Fórmula de Newton-Cotes*
Nombradas así por *Isaac Newton* y *Roger Cotes*, en las cuales se evalúa la función en puntos equidistantes, para así hallar un valor aproximado de la integral. Cuanto más intervalos se divida la función más preciso será el resultado.

*Regla del Trapecio Simple y Compuesto*
La regla del trapecio es la primera regla cerrada del Newton-Cotes. 
Gráficamente:
![Regla De Los Trapecios](https://userscontent2.emaze.com/images/514d0b1f-1b44-412c-b275-a762667c3dc1/ecab57c3-f717-4c1f-8641-d700e8303044png)
Donde: $P_1(a,f(a))$ y $P_2(b,f(b))$. 

Si utilizamos un polinomio $p(x)$ de primer grado como una aproximación de la función, es decir, $p(x)=f(a)\frac{x-b}{a-b}+f(b)\frac{x-a}{b-a}$.

El cal equivale a $p(x)=f(a)+\frac{f(b)-f(a)}{b-a}(x-a)$ , $f(x)=mx+b$.

El área bajo esta linea recta es una aproximación del área bajo la curva entre los limites $a$ y $b$.  
$\int^b_af(x)d_x\approx\int^b_a(f(a)+\frac{f(b)-f(a)}{b-a}(x-a))d_x$

$\approx[f(a)+\frac{f(b)-f(a)}{b-a}\frac{(x-a)^2}{2}]^b_a$

$\approx(b-a)\frac{f(a)+f(b)}{2}$

*Método de Simpson*
También llamada *Regla de Kepler*, es un método de integración numérica que se utiliza para obtener la aproximación de la integral: 

$\int^b_af(x)d_x\approx\frac{b-a}{6}[(f(a)+4f(\frac{a+b}{2})+f(b)]$

Consideremos el polinomio interpolante de *orden 2* $P_2(x)$, que aproxima la función integrando $f(x)$ entre los nodos $x_0=a$, $x_1=b$ y $m=(\frac{a+b}{2})$.

La expresión de ese polinomio interpolante, espesado a través de la interpolación polinómica de *Lagrange* es:

$P_2(x)=f(a)\frac{(x-m)(x-b)}{(a-m)(a-b)}+f(m)\frac{(x-a)(x-b)}{(m-a)(m-b)}+f(b)\frac{(x-a)(x-a)}{(b-a)(b-a)}$

Así la integral buscada $I=\int^b_af(x)d_x$

Es equivalente a $I=\int^b_aP_2(x)d_x+Término De Error=\frac{b-a}{6}[f(a)+4f(m)+f(b)]+\varepsilon(f)$.

Donde $\varepsilon(f)$ es el *Termino de Error*, por lo tanto se puede aproximar a como: 

$\int^b_af(x)d_x\approx\frac{b-a}{6}{6}[f(a)+4f(m)+f(b)]+$

**Tipos de Formulas de *Newton-Cotes***
**ABIERTAS:**
Se usan los nodos $x=x_0+ih$ para cada $i=0,1,2,...,n$, donde $h=\frac{b-a}{n+2}$ ^ $x_0=a+h$
Esto implica que $x_n=b-h$
Si marcamos los puntos extremos tomando $x_{-1}=a$ y $x_{n+1}=b$

Las formulas se transforman en:
$\int^b_af(x)d_x\approx\int^{x_{n+1}}_{-1}f(x)d_x\approx\sum^n_{i=0}a_if(x_i)$

Donde $a_i=\int^b_aL_i(x)d_x$

$\sum^3_{i=0}a_if(x_i)=a_0f(x_0)+a_1f(x_1)+a_2f(x_2)+a_3f(x_3)$

**CERRADAS:**

 - Regla del Trapecio para $N=1$
$\int^{x_1}_{x_0}f(x)d_x\approx\frac{h}{2}[f(x_0)+f(x_1)]-\frac{h^3}{12}f^{''}(\xi)$ , $x_0<\xi<x_1$.  
 - Regla de Simpson para $N=2$
$\int^{x_1}_{x_0}f(x)d_x\approx\frac{h}{3}[f(x_0)+4f(x_1)+f(x_2)]-\frac{h^3}{90}f^{(4)}(\xi)$ , $x_0<\xi<x_2$.  
 
- Regla de Simpson Tres Octavos
$\int^{x_3}_{x_0}f(x)d_x\approx\frac{3h}{8}[f(x_0)+3f(x_1)+3f(x_2)+f(x_3)]-\frac{3h^3}{80}f^{(4)}(\xi)$ , $x_0<\xi<x_3$.  
 - $N=4$
 $\int^{x_4}_{x_0}f(x)d_x\approx\frac{2h}{45}[7f(x_0)+32f(x_1)+12f(x_2)+32f(x_3)+7f(x_4)]-\frac{-8h^7}{945}f^{(6)}(\xi)$ , $x_0<\xi<x_4$.  
