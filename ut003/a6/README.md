 <center>

# TÉCNICAS DE EVASIÓN


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

En esta práctica vamos a realizar técnicas de evasión con archivos maliciosos. 

#### ***Objetivos***. <a name="id2"></a>

El objetivo es subir el archivo malicioso a VirusTotal con el fin de que gracias a las técnicas de evasión el programa no los pueda detectar. 

#### ***Material empleado***. <a name="id3"></a>

El material empleado es una MV de Kali Linux como atacante y otra MV Windows como víctima. 

#### ***Desarrollo***. <a name="id4"></a>

En primer lugar, vamos a listar los ***encoders*** que nos proporciona ***msfvenom***.

![](img/1.png)

Posteriormente, vamos a crear un ***payload*** con ***msfvenom*** con el nombre de "meterpreter.exe". 

![](img/2.png)

Del mismo modo, vamos a realizar el mismo proceso pero aplicando un filtro para silenciar el archivo, es decir, para que no sea tan fácil de detectar ante un antivirus. 

![](img/3.png)

Como podemos apreciar, los dos archivos se han creado correctamente. 

![](img/4.png)

Si pasamos los archivos por ***VirusTotal*** debería de haber una diferencia entre los mismos, ya que el filtro de silencio que hemos aplicado debería de dificultar que nos detecte el archivo malicioso.

Spoiler: No funciona. 

![](img/5.png)

![](img/6.png)

Posteriormente, descargamos ***Putty*** en nuestra MV. 

![](img/7.png)

Una vez descargado, procedemos a incluirlo en los archivos de ***Metaesploit***. 

![](img/8.png)

Otra opción que podemos tomar en cuenta en la creación de un ***Payload*** a través de meterpreter usando un filtro silencioso como se adjunta a continuación. 

![](img/9.png)

Al igual que la práctica anterior, usamos ***msfconsole*** con el exploit de ***handler***, definiendo nuestra IP y el puerto 80. 

![](img/10.png)

Una vez realizado, vamos a crear un servidor mediante ***python3*** para descargar el archivo malicioso en la MV de Windows. 

![](img/11.png)

![](img/12.png)

Una vez la víctima descargue y ejecute el archivo, se nos mostrará una sesión de ***meterpreter*** con acceso total a la máquina. 

![](img/13.png)

![](img/14.png)

---

Por otro lado, vamos a practicar las técnicas de evasión, es decir, vamos a ocultar esos ***payloads*** creados para que el sistema no los pueda detectar. 
Para ello, vamos a instalar ***veil***.

![](img/15.png)

![](img/17.png)

Una vez instalado y ejecutado el programa, seleccionamos la opción "Evasion". 

![](img/18.png)

A continuación, listamos los ***payloads***. 

![](img/19.png)

![](img/20.png)

Y hacemos uso del siguiente ***payload***.

![](img/21.png)

![](img/22.png)

Posteriormente, establecemos la dirección IP y el puerto, el cual será el 80 en este caso. 

![](img/23.png)

Y finalmente generamos el archivo.

![](img/24.png)

![](img/25.png)

Si lo pasamos por ***VirusTotal*** debería de haber una mejoría respecto a los archivos anteriores. 

![](img/26.png)

---

Otro programa del que podemos hacer uso para la evasión de archivos es ***Shellter***. 

![](img/27.png)

A continuación, definimos el archivo que queremos evadir. 

![](img/28.png)

![](img/29.png)

Finalmente, seleccionamos el ***payload*** a ejecutar y el puerto, así como la dirección IP. 

![](img/30.png)

![](img/31.png)

Y si pasamos el archivo por ***VirusTotal*** debería de haber una mejoría respecto a los archivos anteriores. 

![](img/32.png)

#### ***Conclusiones***. <a name="id5"></a>

 Esta práctica nos sirve para ocultar los archivos maliciosos, algo útil desde el lado del atacante, pero el usuario es el principal perjudicado. Es por ello que debemos tener cuidado las fuentes desde las que descargamos nuestros archivos. 


