---
layout: post
title:  "Unidad Fundamental"
date:   2020-09-10 18:51:43 -0400
categories: rpf
tag: 1
---

*La unidad Fundamental*

Normalización de un numero: un número **“X”** está escrito en su forma normalizada si **“X”** está escrito en la siguiente forma: {% katex display %} x= \delta (u.d_1d_2d_3...d_p)_b. b^e{% endkatex %}

Donde  {% katex %}\delta{% endkatex %} es el signo {% katex %}(+1){% endkatex %} si es positivo; {% katex %}(-1){% endkatex %} si es negativo, para {% katex %}0 \leq d_i \leq b - 1{% endkatex %} siendo {% katex %}d_i \neq 0{% endkatex %} y {% katex %}e{% endkatex %} es la característica. Por su puesto lo ubicado dentro del paréntesis es la mantisa.

La mantisa denota: {% katex %}\frac{d_1}{b_1}...+\frac{d_p}{b_p}{% endkatex %} , es decir su parte fraccionaria. 

El entero {% katex %}P{% endkatex %} denota la cantidad de dígitos de precisión y {% katex %}e{% endkatex %} el entero tal que esta: {% katex %}L\neq e \neq U{% endkatex %}  siendo {% katex %}L{% endkatex %} el exponente más pequeño que pueda tomar y {% katex %}U{% endkatex %} el más grande.

![3](/assets/images/3.png)


Los números en punto flotante llamados también números reales, tienen decimales intercalados.
Tales números almacenan y procesan en sus formas exponenciales y binarios. 
La localización se memoria se divide comúnmente en 3 campos o bloques de bits. 
Un campo, el primer bit, se reserva para el primer número. Un segundo campo para el exponente del número y el ultimo campo para la mantisa. 

*Ejemplo:*
Representa el número -0,00523 en una palabra de 16 bits siendo b=10.

*Solución:* primero hay que normalizar el numero 
{% katex %}-0,00523 = (-1)(0,523)_10 10^2{% endkatex %}


![4](/assets/images/4.png)


 Se pone *“1”* porque el {% katex %}\delta{% endkatex %} es negativo.
Si fuese positivo se coloca *“0”*

