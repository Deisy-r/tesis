---
layout: post
title:  "Integración Númerica"
date:   2020-09-10 18:51:43 -0400
categories: in
tag: 0
---
## INTEGRACIÓN NUMÉRICA

**Fórmula de Newton-Cotes**
Nombradas así por *Isaac Newton* y *Roger Cotes*, en las cuales se evalúa la función en puntos equidistantes, para así hallar un valor aproximado de la integral. Cuanto más intervalos se divida la función más preciso será el resultado.

**Regla del Trapecio Simple y Compuesto**
La regla del trapecio es la primera regla cerrada del Newton-Cotes. 
Gráficamente:
![Regla De Los Trapecios](https://userscontent2.emaze.com/images/514d0b1f-1b44-412c-b275-a762667c3dc1/ecab57c3-f717-4c1f-8641-d700e8303044png)
Donde: {% katex %}P_1(a,f(a)){% endkatex %} y {% katex %}P_2(b,f(b)){% endkatex %}. 

Si utilizamos un polinomio {% katex %}p(x){% endkatex %} de primer grado como una aproximación de la función, es decir, {% katex %}p(x)=f(a)\frac{x-b}{a-b}+f(b)\frac{x-a}{b-a}{% endkatex %}.

El cual equivale a {% katex %}p(x)=f(a)+\frac{f(b)-f(a)}{b-a}(x-a){% endkatex %} , {% katex %}f(x)=mx+b{% endkatex %}.

El área bajo esta linea recta es una aproximación del área bajo la curva entre los limites {% katex %}a{% endkatex %} y {% katex %}b{% endkatex %}.

{% katex display %}\int^b_af(x)d_x\approx\int^b_a(f(a)+\frac{f(b)-f(a)}{b-a}(x-a))d_x{% endkatex %}

{% katex display %}\approx[f(a)+\frac{f(b)-f(a)}{b-a}\frac{(x-a)^2}{2}]^b_a{% endkatex %}

{% katex display %}\approx(b-a)\frac{f(a)+f(b)}{2}{% endkatex %}

**Método de Simpson**
También llamada *Regla de Kepler*, es un método de integración numérica que se utiliza para obtener la aproximación de la integral: 

{% katex display %}\int^b_af(x)d_x\approx\frac{b-a}{6}[(f(a)+4f(\frac{a+b}{2})+f(b)]{% endkatex %}

Consideremos el polinomio interpolante de *orden 2* {% katex %}P_2(x){% endkatex %}, que aproxima la función integrando {% katex %}f(x){% endkatex %} entre los nodos {% katex %}x_0=a{% endkatex %}, {% katex %}x_1=b{% endkatex %} y {% katex %}m=(\frac{a+b}{2}){% endkatex %}.

La expresión de ese polinomio interpolante, espesado a través de la interpolación polinómica de *Lagrange* es:

{% katex display %}P_2(x)=f(a)\frac{(x-m)(x-b)}{(a-m)(a-b)}+f(m)\frac{(x-a)(x-b)}{(m-a)(m-b)}+f(b)\frac{(x-a)(x-a)}{(b-a)(b-a)}{% endkatex %}

Así la integral buscada {% katex %}I=\int^b_af(x)d_x{% endkatex %}

Es equivalente a {% katex %}I=\int^b_aP_2(x)d_x+Término De Error=\frac{b-a}{6}[f(a)+4f(m)+f(b)]+\varepsilon(f){% endkatex %}.

Donde {% katex %}\varepsilon(f){% endkatex %} es el *Termino de Error*, por lo tanto se puede aproximar a como: 

{% katex display %}\int^b_af(x)d_x\approx\frac{b-a}{6}{6}[f(a)+4f(m)+f(b)]+{% endkatex %}

**Tipos de Formulas de *Newton-Cotes***
**ABIERTAS:**
Se usan los nodos {% katex %}x=x_0+ih{% endkatex %} para cada {% katex %}i=0,1,2,...,n{% endkatex %}, donde {% katex %}h=\frac{b-a}{n+2}{% endkatex %} ^ {% katex %}x_0=a+h{% endkatex %}
Esto implica que {% katex %}x_n=b-h{% endkatex %}

Si marcamos los puntos extremos tomando {% katex %}x_{-1}=a{% endkatex %} y {% katex %}x_{n+1}=b{% endkatex %}

Las formulas se transforman en:
{% katex display %}\int^b_af(x)d_x\approx\int^{x_{n+1}}_{-1}f(x)d_x\approx\sum^n_{i=0}a_if(x_i){% endkatex %}

Donde {% katex %}a_i=\int^b_aL_i(x)d_x{% endkatex %}

{% katex display %}\sum^3_{i=0}a_if(x_i)=a_0f(x_0)+a_1f(x_1)+a_2f(x_2)+a_3f(x_3){% endkatex %}

**CERRADAS:**

 - Regla del Trapecio para {% katex %}N=1{% endkatex %}
{% katex display %}\int^{x_1}_{x_0}f(x)d_x\approx\frac{h}{2}[f(x_0)+f(x_1)]-\frac{h^3}{12}f^{''}(\xi){% endkatex %} , {% katex %}x_0<\xi<x_1{% endkatex %}.  
 - Regla de Simpson para {% katex %}N=2{% endkatex %}
{% katex display %}\int^{x_1}_{x_0}f(x)d_x\approx\frac{h}{3}[f(x_0)+4f(x_1)+f(x_2)]-\frac{h^3}{90}f^{(4)}(\xi){% endkatex %} , {% katex %}x_0<\xi<x_2{% endkatex %}.  
 
- Regla de Simpson Tres Octavos
{% katex display %}\int^{x_3}_{x_0}f(x)d_x\approx\frac{3h}{8}[f(x_0)+3f(x_1)+3f(x_2)+f(x_3)]-\frac{3h^3}{80}f^{(4)}(\xi){% endkatex %} , {% katex %}x_0<\xi<x_3{% endkatex %}.  
 - {% katex %}N=4{% endkatex %}
 {% katex display %}\int^{x_4}_{x_0}f(x)d_x\approx\frac{2h}{45}[7f(x_0)+32f(x_1)+12f(x_2)+32f(x_3)+7f(x_4)]-\frac{-8h^7}{945}f^{(6)}(\xi){% endkatex %} , {% katex %}x_0<\xi<x_4{% endkatex %}.  
