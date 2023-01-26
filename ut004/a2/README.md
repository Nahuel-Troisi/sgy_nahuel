<center>

# VPN - WIN SERVER 2016


</center>

***Nombre:*** Nahuel Ivan Troisi

<br>

***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

## ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


## ***Introducción***. <a name="id1"></a>

Vamos a crear un servicio de conexiones VPN. 

## ***Objetivos***. <a name="id2"></a>

Crear el servicio de conexiones VPN y comprobar que funciona. 

## ***Material empleado***. <a name="id3"></a>

Para la configuración del servicio VPN vamos a utilizar una MV de Windows Server, mientras que para las comprobaciones pertinentes usaremos una MV con Windows 7. 

## ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a comprobar que nuestra MV de Windows Server posee una dirección IP adecuada a la red que nos encontramos. 

![](img/1.PNG)

Posteriormente, vamos a añadir un nuevo rol en el servivor, concretamente el de ***"Acceso Remoto"***.

![](img/2.PNG)

Del mismo modo, instalamos las características necesarias para que el servicio funcione correctamente. 

![](img/3.PNG)

Una vez instalado el servicio, debería de quedar de la manera siguiente. 

![](img/4.PNG)

Posteriormente, vamos a proceder a configurar nuestra VPN. 

![](img/5.PNG)

Dentro de la misma, seleccionamos la opción ***"Personalizada"***. 

![](img/6.PNG)

Del mismo modo, elegimos las opciones de ***"Acceso a VPN"***.

![](img/7.PNG)

Una vez realizada la configuración, debería de quedar de la manera siguiente.

![](img/8.PNG)

Ahora vamos a pasar a nuestra MV de Windows 7, para proceder a conectarnos a la VPN. 

![](img/10.PNG)

Y probamos que funciona la conexión, aunque en este caso, nos da error y no conecta. 

![](img/11.PNG)

## ***Conclusiones***. <a name="id5"></a>

La práctica es sencilla de realizar si seguimos el tutorial del Campus, aunque personalmente no me ha funcionado pese a seguir los mismos pasos. 