<center>

# PHISHING - SET


</center>

***Nombre:*** Nahuel Ivan Troisi
<br>
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

En esta práctica vamos a clonar un sitio web con la finalidad de ganar acceso al usuario y contraseña de la víctima.

#### ***Objetivos***. <a name="id2"></a>

Clonar la página web y conseguir sus credenciales. 

#### ***Material empleado***. <a name="id3"></a>

Hemos empleado la MV de Kali Linux tanto para el uso de SET como para elaborar el informe. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a inicar el servicio de SET (Social Engineering Toolkit).

![](img/9.png)

Una vez arrancado el servicio, vamos a elegir de todas las opciones, la que se encuentra en primer lugar, es decir, vamos a realizar ataques de ingeniería
social. 

![](img/1.png)

Posteriormente, vamos a utilizar el ataque basado en vectores para las páginas web. 

![](img/2.png)

El paso siguiente es seleccionar el método de ataque web. 

![](img/3.png)

Seleccionamos la opción de clonar un sitio web. 

![](img/4.png)

El sitio web en cuestión es la web de Binance, el mayor exchange de criptomonedas del mundo, por lo que deberemos de copiar la URL.

![](img/5.png)

Una vez copiada la dirección URL, vamos a pegarla en nuestro SET. 

![](img/6.png)

El programa procederá a clonar la página web y nos informará cuando la víctima haya accedido a la misma, además de facilitarnos el usuario y la contraseña. 

![](img/7.png)


#### ***Conclusiones***. <a name="id5"></a>

Me ha resultado una práctica bastante sencilla, ya que el programa lo automatiza todo. No obstante, la web carece de HTTPS, por lo que es fácil identificar
que la web es falsa o poco fiable. 
