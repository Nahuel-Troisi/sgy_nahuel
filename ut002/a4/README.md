<center>

# CIFRADO ASIMÉTRICO - GPG


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

En esta práctica vamos a cifrar una serie de archivos, los cuales se podrán descifrar únicamente con nuestra clave pública. 

#### ***Objetivos***. <a name="id2"></a>

La finalidad de esta práctica es aprender a crear unas claves público-privadas y hacer uso de los archivos encriptados, los cuales sólo se pueden leer
gracias a la clave pública de su creador. 

#### ***Material empleado***. <a name="id3"></a>

Para la realización de la práctica hemos utilizado una MV con Ubuntu 22 y para el informe hemos recurrido a la MV de Kali Linux. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a generar una clave público-privada mediante GPG, la cual consta de tipo RSA a RSA, una longitud de 4096 bits y la caducidad de la misma
es nula. 

![](img/1.png)

![](img/2.png)

Una vez creada, nos solicitará una contraseña para poder proteger nuestra clave. En este caso hemos definido una muy sencilla "12345678A", pero podemos
utilizar una diferente si se desea. 

![](img/3.png)

Si hacemos uso del comando "gpg -k" podremos visualizar las características de nuestra clave recién creada. 

![](img/4.png)

Ahora vamos a exportar nuestra clave al formato "asc". 

![](img/5.png)

Si hacemos uso de "cat" para comprobar el resultado de la exportación, nos debería de aparecer lo siguiente. 

![](img/6.png)

Lo que acabamos de ver es nuestra clave pública encriptada. Si queremos enviarnos mensajes con otro usuario, necesitaremos un archivo similar. En este caso
mi compañero Cristian me ha enviado su clave pública encriptada, la cual vamos a copiar en un archivo de texto y lo vamos a denominar "clave.cristian.gpg.asc". 

![](img/7.png)

Y quedaría de la siguiente manera. 

![](img/8.png)

Ahora vamos a importar la clave de Cristian, la cual hemos copiado anteriormente en el archivo de texto. 

![](img/9.png)

Posteriormente, nosotros vamos a crear un archivo de texto con un mensaje en su interior, con la intención de encriptarlo y que Cristian lo pueda descifrar
y leer gracias a la clave pública que le hemos proporcionado. 

![](img/10.png)

Encriptamos el archivo en cuestión. 

![](img/11.png)

Una vez encriptado quedaría tal que así. 

![](img/12.png)

A continuación, Cristian nos ha mandado un mensaje encriptado, el cual es el siguiente. 

![](img/13.png)

Procedemos a descifrarlo gracias a su clave pública. 

![](img/14.png)

Introducimos la clave que definimos al principio de la práctica. 

![](img/15.png)

Y el mensaje de Cristian es el siguiente. 

![](img/16.png)

#### ***Conclusiones***. <a name="id5"></a>

El cifrado de archivos ha estado una práctica muy interesante. De este modo podemos ampliar el nivel de seguridad de nuestros archivos personales
y podemos decidir quien tiene acceso a los mismos. 

