<center>

# WIFIRADIUS - PFSENSE


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

En esta práctica vamos a configurar ***PFSENSE*** con el fin de restringir el acceso a la web si el usuario no valida sus credenciales o no tiene acceso a las mismas.  

#### ***Objetivos***. <a name="id2"></a>

Restringir el acceso al personal no autorizado. 

#### ***Material empleado***. <a name="id3"></a>

Para esta práctica hemos usado dos MV, una con ***PFSENSE*** y otra con Ubuntu para realizar las comprobaciones. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a configurar correctamente ambas MV virtuales. En el caso de "PFSENSE" vamos a añadir dos adaptadores de red, configurados en "Red Interna" y "NAT" respectivamente. 

![](img/1.png)

Del mismo modo, realizamos el mismo proceso con la MV de Ubuntu, pero en este caso se le asignará un único adaptador de red en modo "Red Interna". 

![](img/2.png)

Una vez realizadas estas configuraciones previas, procedemos a instalar "PFSENSE" en la MV siguiendo los pasos que se adjuntan en las imágenes. 

![](img/3.png)

![](img/4.png)

![](img/5.png)

Una vez finalizada la instalación, al arrancar de nuevo la MV se cargará el sistema y se configurará de forma automática en función de nuestros adaptadores de red y como éstos se encuentren configurados. 
En este caso, debería de aparecernos ambos adaptadores de red, configurados como se adjunta en la imagen. 

![](img/6.png)

En nuestra MV Ubuntu, vamos a añadir el DNS de forma manual, apuntando al la dirección que nos proporciona "PFSENSE", es decir, ***192.168.1.1***. 
También podemos asignar una IP fija si lo deseamos, aunque no es del todo necesario. 

![](img/7.png)

Para comprobar que el servicio está activo, vamos a acceder a la IP ***192.168.1.1*** desde la MV Ubuntu. Por defecto el usuario es "admin" y la contraseña "pfsense".

![](img/8.png)

A continuación, vamos a configurar "PFSENSE" siguiendo los pasos que se adjuntan en las imágenes siguientes para asegurarnos de su correcto funcionamiento. 

![](img/9.png)

![](img/10.png)

Una vez realizado, en nuestra MV Ubuntu vamos a proceder a asignar un DNS y dirección IP de forma automática para comprobar que hemos configurado correctamente el servicio. 

![](img/11.png)

Si hacemos uso de un ***ip a***, veremos que nos asigna una dirección válida en la red. 

![](img/12.png)

Una vez realizado este paso, vamos a instalar el paquete de "wifiradius". 

![](img/13.png)

A continuación, vamos a configurar el uso del mismo, siguiendo los pasos que se adjuntas en las imágenes. 

![](img/14.png)

![](img/15.png)

![](img/16.png)

![](img/17.png)

![](img/18.png)

![](img/19.png)

![](img/20.png)

![](img/21.png)

![](img/22.png)

![](img/23.png)

![](img/24.png)

![](img/25.png)

![](img/26.png)

Una vez configurado todo, si intentamos acceder a cualquier página web, nos saltará este mensaje de autenticación, lo que quiere decir que el servicio funciona correctamente. 

![](img/27.png)

Una vez validadas las credenciales, ya podemos navegar con normalidad. 

![](img/28.png)

#### ***Conclusiones***. <a name="id5"></a>

La práctica aunque es sencilla de realizar si seguimos los pasos, puede dar pie a muchos errores de conexión o de configuración por parte de la MV de "PFSENSE", la cual se soluciona reinciando el sistema (a veces incluso en más de una ocasión). No obstante, es interesante el uso de la restricción a nivel de red mediante autenticación. 
