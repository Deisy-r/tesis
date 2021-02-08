---
layout: post
title:  "Método de Taylor"
date:   2020-09-10 18:51:43 -0400
categories: senluv
tag: 4
---

## Teorema de Taylor

Supongamos que {% katex %}f\in C^n[a,b]{% endkatex %} y {% katex %}f^{n+1}{% endkatex %} existe en {% katex %}[a,b]{% endkatex %}. Sea {% katex %}x_o\in[a,b]{% endkatex %} para todo {% katex %}x\in[a,b]{% endkatex %}, existe {% katex %}\xi(x){% endkatex %} entre {% katex %}x_0^x{% endkatex %}

{% katex display %}f(x)=P_n(x)+R_n(x){% endkatex %}

Donde
{% katex display %}P_n(x)=f(x_0)+f'(x_0)(x-x_0)+\frac{f''(x_0)}{2!}(x-x_0)+...+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n={% endkatex %}
{% katex display %}R_n(x)=\frac{f^{(n+1)}(\xi(x))}{n+1!}(x-x_0)^{n+1}{% endkatex %}
{% katex display %}=\sum^n_{k=0} \frac{f^{(k)}(x_0)}{k!}(x-x_0)^k{% endkatex %}
________
Suponga que la función {% katex %}f{% endkatex %} es continuamente diferenciable dos veces en el intervalo cerrado {% katex %}[a,b]{% endkatex %}, es decir, {% katex %}f\in C^2[a,b]{% endkatex %}, sea {% katex %}x̄\in[a,b]{% endkatex %}, una aproximación a {% katex %}P{% endkatex %}, tal que {% katex %}f'(x̄)\neq0{% endkatex %} y {% katex %}|x̄-p|{% endkatex %} es "pequeño". 

{% katex display %}f(x)=f(x̄)+(x-x̄)f'(x̄)+\frac{(x-x̄)^2}{2}f'(\xi(x)), {% endkatex %} {% katex %}x<\xi(x)<x̄{% endkatex %}
como {% katex %}f(p)=0{% endkatex %}
{% katex display %}0=f(x̄)+(p-x̄)f'(x)+\frac{(p-)^2}{2}f'(\xi(x)),{% endkatex %} 
{% katex display %}f(x̄)+(p-x̄)f'(x̄) \approx0{% endkatex %}
{% katex display %}f(x̄)+pf'(x̄)-x̄f'(x̄) \approx0{% endkatex %}
{% katex display %}pf'(x̄)\approx x̄f'(x̄)-f(x̄){% endkatex %}
{% katex display %}p\approx \frac{x̄f'(x̄)-f(x̄)}{f'(x̄)}{% endkatex %}
{% katex display %}p\approx \frac{x̄f'(x̄)}{f'(x̄)}-\frac{f(x̄)}{f'(x̄)}{% endkatex %} {% katex %}\approx x̄-\frac{f(x̄)}{f'(x̄)}{% endkatex %}


Una sucesión {% katex %}{p_n}{% endkatex %} definida por:
{% katex display %}p_n=p_{n-1}\frac{f(p_{n-1})}{f'(p_{n-1)}}{% endkatex %} donde {% katex %}n>1{% endkatex %}

**Teorema**
Sea {% katex %}f\in C^2[a,b]{% endkatex %}. Si {% katex %}p\in[a,b]{% endkatex %}, es tal que {% katex %}f(p)=0{% endkatex %} y {% katex %}f(p)\neq0{% endkatex %}, entonces existe {% katex %}\delta>0{% endkatex %} tal que el *Método de Newton* genrea una sucesión {% katex %}(p)^\infty n=1{% endkatex %} que converge a {% katex %}p{% endkatex %} para cualquier aproximación inicial {% katex %}p_0 \in[p-\delta_1p+\delta]{% endkatex %}
