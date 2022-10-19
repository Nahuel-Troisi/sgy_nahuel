
<center>

# COPIAS DE ARCHIVOS - RSYNC


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

Vamos a realizar una práctica con RSync para copiar archivos de una MV a otra. 

#### ***Objetivos***. <a name="id2"></a>

El objetivo es copiar varios archivos de una MV a otra, además de comprobar si, en caso de borrar o editar los archivos, los cambios se hacen efectivos. 

#### ***Material empleado***. <a name="id3"></a>

En este caso hemos hecho uso de dos MV con Ubuntu para realizar las comprobaciones de RSync, no obstante, para realizar el informe hemos hecho uso de una MV
con Kali Linux. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a configurar las dos máquinas virtuales con dos IP que sean fáciles de reconocer, por lo que le vamos a asignar las direcciones
"172.19.99.1" y "172.19.99.2" respectivamente. 

![](img/1.png)

![](img/2.png)

A continuación, vamos a crear la carpeta "datos_nahuel" en la MV 1, donde vamos a almacenar 100 archivos. 

![](img/3.png)

![](img/4.png)

Una vez realizado este proceso, vamos a aplicar "Rsync" para copiar estos archivos a la otra MV. 

![](img/5.png)

Comprobamos que se han copiado correctamente. 

![](img/6.png)

Posteriormente, vamos a editar el fichero "1" y vamos a comprobar si se aplican los cambios en la otra MV al realizar "RSync". 

![](img/7.png)

![](img/8.png)

![](img/9.png)

Como podemos comprobar, "RSync" sincroniza los cambios realizados entre las dos MV. 

<br>

Ahora vamos a probar a borrar el archivo "100" y comprobar si se hace el mismo proceso en la MV 2. 

![](img/10.png)

![](img/11.png)

No obstante, el fichero sigue apareciendo en la MV 2. 

<br>

Para que los cambios se hagan efectivos debemos usar el parámetro "--delete" al final del comando.

![](img/12.png)

Si provamos a hacer una comprobación nuevamente, veremos que el archivo "100" se ha borrado correctamente. 

![](img/13.png)

Finalmente, vamos a crear la carpeta "system.d_nahuel" en la MV 2, la cual vamos a sincronizar con el directorio "/etc/systemd" de la MV 1 con el parámetro
"-r". 

![](img/14.png)

![](img/15.png)

#### ***Conclusiones***. <a name="id5"></a>

Esta práctica ha sido mas sencilla y rápida que la anterior, ya que únicamente debíamos hacer uso de un par de comandos y hacer las respectivas comprobaciones. 
