---
layout: post
title:  "Representación Entera"
date:   2020-09-10 18:51:43 -0400
categories: rpf
tag: 2
---
**REPRESENTACION ENTERA**

Los enteros o números en punto fijo son números que no tienen punto decimal. Un entero **J** se representa en la memoria de un computador por medio de su forma binaria si son positivos y por medio de su complemento a **2** de su valor absoluto. 


*Ejemplo:*
{% katex display %}
4  2  3 = 1 1 0 1 0 0 1 1 1
{% endkatex %}

![entera](/assets/images/entera.png)

 El computador almacena {% katex %}-423{% endkatex %} en una localización de memoria, tomando el complemento a {% katex %}1{% endkatex %} de la anterior representación {% katex %}423{% endkatex %} y sumándole un {% katex %}1{% endkatex %} el computador puede saber si un entero **J** en la memoria es positivo o negativo minando el primer dígito. 


Si {% katex %}J=0\rightarrow + {% endkatex %}


Si {% katex %}J=1\rightarrow - {% endkatex %}
