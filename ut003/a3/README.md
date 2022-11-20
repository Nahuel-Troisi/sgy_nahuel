<center>

# METAESPLOITABLE 2 - VULNERABILIDADES


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

Vamos a explotar las vulnerabilidades de una MV víctima con el fin de ganar acceso a la misma. 

#### ***Objetivos***. <a name="id2"></a>

Ganar acceso a la MV y por ende, a los datos que almacena. 

#### ***Material empleado***. <a name="id3"></a>

Hemos empledo una MV de Kali Linux para poder hacer los ataques, además de poder redactar el informe y como máquina víctima hemos hecho uso de Metaesploitabe 2. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a activar el servicio "postgresql" con el fin de dejar registrado todos los escaneos que vayamos realizando. 

![](img/1.png)

Posteriormente, vamos a abrir Metaesploid. 

![](img/2.png)

Una vez cargado, vamos a realizar un escaneo de la MV, obteniendo los resultados que se adjuntan a contiunuación. 

![](img/3.png)

![](img/4.png)

Como podemos ver, el puerto 3306 (donde se ejecuta MYSQL) se encuentra abierto, por lo que vamos a proceder a atacar por ahí. 
Desde la terminal de Metasploid, vamos a probar a conectarnos a la base de datos, la cual, si no está configurada correctamente, puede carecer de contraseña. 

![](img/5.png)

Como podemos ver, hemos podido acceder sin problemas y tenemos acceso a toda la información. 

![](img/6.png)

Otro puerto que se encuentra abierto es el 21, donde tenemos el servicio FTP. 

![](img/7.png)

Al igual que en el caso anterior, desde Metaesploid vamos a introuducir la IP de la máquina víctima y vamos a ejecutar un exploit que nos debería de ganar acceso
a la MV. 

![](img/8.png)

Y como podemos observar, estamos dentro. 

![](img/9.png)

#### ***Conclusiones***. <a name="id5"></a>

Una práctica bastante guiada y fácil de seguir, quizás sería más recomendable algo similar pero careciendo de los pasos a seguir, para poder realizar el trabajo
de investigación por uno mismo, ya que hay muchas formas de acceder a esta MV. 

