# Documentacion

## Que es una instancia?
Las instancias de uso general brindan una combinación equilibrada de recursos informáticos, de memoria y de red. Además, pueden usarse para distintas cargas de trabajo. Estas instancias son ideales para las aplicaciones que usan estos recursos en partes iguales, como los servidores web y los repositorios de código. 
## Instancia-1
Primero lanzaremos una instacia  arruba a la dererha de la captura de la parte inferior esta visualizada.
![Primer Paso](/img/Lanzar.png)
Eligiremos el Ubuntu Server 20.04 para nuestro server 
![Segundo Paso](/img/TipoServer.png)
En el tipo de instancia nos saldra los tipops que hay asique escogeremos el predeterminado
![Tercer Paso](/img/TipoInstancia.png)
En este paso cambiaremos el almacenamineto por 30 , que en la captura nos saldra seleccionado pero no esta cambiado
![Cuarto Paso](/img/Storage.png)
Daremos siguiente en los tags no hay q tocar nada
![Quinto Paso](/img/Addtags.png)
ponemos la 0.0.0.0 porque abarca todos los rangos de las ips
![Sexto Paso](/img/ConfigureGroup.png)
Ahora instalaremos la clave que en este caso lo llamamos clave1.pem , lo guardaremos en un lugar que nos acordemos y clicamos en el boton azul que pone "Launch Instances"
![Septimo Paso](/img/Clave.png)
Clicamos en los numeros de la instacia 
![Novemo Paso](/img/InstanciaCreada.png)
Nos abrira un apartado en el cual entramos al Cliente SSH
![Octavo Paso](/img/ConectarseInstancia.png)
Y ahora vamos al archivo del la clave  la seleccionamos y entramos en el Git Bash here
![Noveno Paso](/img/ClaveGitbash.png)
Nos abrirala terminal y monemos los siguientes comando s para entrar la cual tambien los saldran el la captura donde entramos en el apartado cliente SSH
![Decimo Paso](/img/EntramosConLaClave.png)

## Instalacion Apache
Vamos a la consola y ponemos el siguiente comando
![Primer Paso](/img/Apache1.png)
Entramos en reglas de entrada  y añadimos un nuevo tipo que sera el http.
![Segundo Paso](/img/Apache2.png)
Cuando este correcto todo en el navegador pondremos este comando la cual nos dira si esta abierto.
![Tercer Paso](/img/Apache3.png)
Este sera el comando para ver el estado de nuestro apache
este comando se recoge de desde la instancia boton dereche y Coneactar .
"ssh -i "clave1.pem" ubuntu@ec2-34-229-192-78.compute-1.amazonaws.com "
![Cuerto Paso](/img/Apache4.png)

## Instalacion MYSQL
Instalamos el mysql-server 
![Primer Paso](/img/mysql1.png)
Esta captura es la de inicio de el mysql y la del status del mysql
![Segundo Paso](/img/mysql2.png)

## Instalacion PHP
Instalamos el php 
![Primer Paso](/img/php1.png)
El status del php
![Segundo Paso](/img/php2.png)

## Instalacion FTP
Instalamos el Ftp 
![Primer Paso](/img/ftp1.png)
El status del Ftp
![Segundo Paso](/img/ftp2.png)

## IP ELASTICA

## Que es una ip Elastica?
Las direcciones IP elásticas son direcciones IPv4 estáticas diseñadas para la informática en la nube dinámica. Con una dirección IP elástica, puede enmascarar los errores de una instancia o software volviendo a mapear rápidamente la dirección a otra instancia de su cuenta.

## IP ELASTICA 1
 Entramos en el panel de EC2 y nos adentramos en el apartado "Direcciones Ip elasticas"
![Primer Paso](/img/ipelastica1.png)
Entramos en asignar direccion de IP elastica
![Segundo Paso](/img/ipelastica2.png)
Asignamos la ip elastica
![Tercer Paso](/img/ipelastica3.png)
Entramos en Asociar la direccion IP elastica que ser para enlazarlo con la instancia
![Cuarto Paso](/img/ipelastica4.png)
En instacias seleccionamos nuestra insatancia y le damos click al boton naranja de abajo para asociar la instacia a la ip elastica
![Quinto Paso](/img/ipelastica5.png)
Esto es saldra si la ip elastica a sido bien enlazada
![Sexto Paso](/img/ipelastica6.png)

## DNS

## Que es y para que sirve?
Unicamente son unas direcciones que introducimos en nuestra configuración de conexión a Internet y que nos sirven para poder conectarnos y para otros

## Diferentes tipos de DNS 

A = Se usa para traducir nombres de servidores de alojamiento a direcciones IPv4 .

AAAA = Se usa para traducir nombres de hosts a direcciones IPv6.

CNAME = Se usa para crear nombres de servidores de alojamiento adicionales, o alias, para los servidores de alojamiento de un dominio.

NS = Define la asociación que existe entre un nombre de dominio y los servidores de nombres que almacenan la información de dicho dominio.

MX = Asocia un nombre de dominio a una lista de servidores de intercambio de correo para ese dominio.

PTR = Funciona a la inversa del registro A, traduciendo IPs en nombres de dominio. Se usa en el archivo de configuración de la zona DNS inversa.

SOA =  Proporciona información sobre el servidor DNS primario de la zona.

SRV = Es un registro DNS donde se especifica información sobre los servicios disponibles del dominio.

ANY = Toda la información de todos los tipos que exista. (No es un tipo de registro, sino un tipo de consulta)

## Imagen del registro de nuestro servidor


![Primer Paso](/img/dns.png)

Todos tienen un TTL de 300 

¿Qué es el TTL?

TTL (time-to-live, tiempo de vida) es el tiempo durante el que un registro DNS permanece almacenado en la memoria caché de un servidor.

1.-Dirección IP de nuestro dominio
2.-Nombre asociado a la dirección de correo.
3.-Lo rellenamos para evitar el uso indebido del correo electronico.

## Cuantos Servidores DNS Existen

DNS que se encuentran a diferentes niveles, hay 13 servidores DNS mundiales que son los encargados de dar toda la información a los demás servidores.

![Segundo Paso](/img/dns2.png)

A partir del 17/12/2020 11:38 am, el sistema del servidor raíz consta de 1367 instancias operadas por los 12 operadores independientes del servidor raíz.

https://root-servers.org/

![Tercer Paso](/img/dns3.png)

##  Cuantas redirecciones DNS son posibles
 
 Todas las necesarias hasta que encuentre la direccion IP

 ##  ¿Qué son los servidores DNS Raíz?

 Un servidor raíz es un servidor de nombres para la zona raíz del Sistema de nombres de dominio de Internet. Los servidores de nombres raíz son una parte fundamental de Internet, ya que son el primer paso en la traducción de los nombres de host legibles en direcciones IP que se utilizan en la comunicación entre los hosts de Internet.

 ## ¿Para qué montar un servidor si simplemente escribiendo en un fichero la relación IP/Nombre el sistema ya funcionaría?

 Por que puedes conectarte desde otro ordenador escribiendo mi Ip para tener acceso.

 ##  Según lo expuesto, y si en tu configuración de red del sistema operativo solamente posees un servidor DNS, entonces: ¿cuál sería el proceso para encontrar la IP de la dirección web: http://www.debian.org/distrib/netinst?
Nos daria un error de direcccion no encontrada

## - ¿Es posible si dispones de una conexión a Internet con IP dinámica ofrecer servicios en Internet? Es decir, si quieres ofrecer los servicios SND, no dispones de IP estática, esto es, cada vez que te conectas a Internet tu IP, aunque a veces sea la misma, no siempre es la misma. 
Introducimos la dirección URL esa llamada llega al Servidor DNS Principal que hace una consulta al DNS Raiz y responde con la dirección IP y nombre de un servidor DNS del dominio superior .org. 
El servidor vuelve a hacer una consulta pero esta vez al servidor DNS para el dominio .org (superior) que nos responde con la dirección IP y el nombre de los servidores de nombre para debian.org.

## ¿Que es la ICANN?
ICANN es una organización que opera a nivel multinacional/internacional y es la responsable de asignar las direcciones del protocolo IP

ICANN coordina la administración de los elementos técnicos del DNS para garantizar la resolución unívoca de los nombres, de esta manera los usuarios puedan encontrar todas las direcciones IP sin ser repetidas.