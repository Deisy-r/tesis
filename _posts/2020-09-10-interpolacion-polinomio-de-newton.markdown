---
layout: post
title:  "Polinomio Interpolante de Newton"
date:   2020-09-10 18:51:43 -0400
categories: interpolacion
tag: 1
---


Este método es algorítmico y resulta sumamente extenso como en determinados casos, sobre todo cuando se requiere calcular un polinomio interpolador de grado elevado.
Para un polinomio de *n-esimo* orden se requiere de 


{% katex %}(x_0,f(x_0)), (x_1,f(x_1)), ..., (x_n,f(x_n)){% endkatex %}. 

Con la Siguiente formula: 

{% katex display %}P_n(x)=b_0+b_1(x-x_0)+b_2(x-x_0)(x-x_1)+b_n(x-x_0)(x-x_1)...(x-x_{n-1}){% endkatex %}
{% katex display %}P_n(x)=b_0+\sum^n_{i=1}b_i(\pi^{i=1}_{j-1}(x-x_j)){% endkatex %}

Estos coeficientes se calculan mediante diferencias divididas cuya expresión general esta dada por:

{% katex display %}f[x_i,...,x_i+j+1]=\frac {f[x_{i+1},...,x_i+j+1]-f[x_i,...,x_i+j]}{x_i+j+1-x_i}{% endkatex %}

Como se ve en la fórmula, la diferencia dividida se calcula de modo recursivo usando coeficientes anteriores. Una vez se halla realizado cada uno de los cálculos, notara que hay muchas mas diferencias divididas que coeficientes {% katex %}b_i{% endkatex %}. 

El cálculo de todos los términos intermedios debe realizarse simplemente porque son necesarios para poder formar todos los términos finales. 

La construcción del polinomio interpolador son aquellos que involucren a {% katex %}x_0{% endkatex %}. 
{% katex display %}b_0=f[x_0], b_1=f[x_0,x_1],...,b_i=f[x_0,x_1,...,x_i]{% endkatex %}

Con esta notación podemos expresar el polinomio {% katex %}p_n(x){% endkatex %} con:


{% katex display %}p_n(x)=[x_0]+f[x_0,x_1](x-x_0)+f[x_0,x_1,...,x_n](x-x_0)(x-x_1)...(x-x_{n-1}){% endkatex %}

A esta ecuación se conoce con el nombre de *Formula de diferencias Divididas Interpolantes de Newton* 


___
*Ejemplo:* Determine el polinomio Interpolante de Newton que contiene los puntos {% katex %}(-3,9),(5,2),(7,-1),(8,0){% endkatex %}

*Solución:*

![tabla](/assets/images/newton interpolante tabla.png)


Para entender el algoritmo del polinomio interpolante de newton mediante las diferencias divididas, hagamos la construcción por niveles o columnas.

Nivel {% katex %}b_1{% endkatex %}

{% katex display %}b_1=\frac{2-9}{5-(-3)}=\frac{-7}{8},{% endkatex %} 
{% katex display %}\frac{(-1)-2}{7-5}=\frac{-3}{2},{% endkatex %} 
{% katex display %}\frac{0-(-1)}{8-7}=\frac{1}{1}=1{% endkatex %}

Nivel {% katex %}b_2{% endkatex %}

{% katex display %}b_2=\frac{\frac{-3}{2}-\frac{-7}{8}}{7-(-3)}=\frac{\frac{-5}{8}}{10}=\frac{-1}{16},{% endkatex %}
{% katex display %}\frac{1-\frac{-3}{2}}{8-5}=\frac{\frac{5}{2}}{3}=\frac{5}{6}{% endkatex %}

Nivel {% katex %}b_3{% endkatex %} 

{% katex display %}b_3=\frac{\frac{-1}{16}-\frac{5}{6}}{8-(-3)}=\frac{\frac{-43}{48}}{11}=\frac{-43}{528}{% endkatex %}
