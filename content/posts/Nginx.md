---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "NGINX"
---

## Nginx interno {#nginx-interno}

### Configuración

La instalación de Nginx será en la máquina de REDHAT.

Nos conectamos a la máquina mediante SSH. Y luego mediante el agent ssh entramos en la maquina redhat al no poder conectarnos directamente. Lo primero que hare sera instalar el nginx.![][image4]

Ahora deberemos cambiar la configuración de SELinux a 0 para poder evitar cualquier fallo.

![][image5]

Enviamos los documentos html con el comando scp.

![][image6]

Ahora iremos al fichero de configuración de nginx.

En el configuraremos también varios usuarios, siendo los 5 integrantes del grupo (en verdad deberían de ser miembros del departamento de informática).![][image7]

Para poder usar el html tendremos que descargar la herramienta zip, esto es debido a que redhat no la tiene por defecto.![][image8]![][image9]

Ahora hay que crear la carpeta donde estarán nuestros html.![][image10]

Para que todo funcione ahora deberemos activar de manera por defecto nginx.

Ahora en caso de que se apague el servidor nginx se iniciará sin tener que usar el start.![][image11]

Para acceder tendremos que primero conectarnos por vpn. Las reglas de entrada de AWS ya están cambiadas.![][image12]

### HTTPS {#https}

Tenemos que crear un par de claves para añadirlo en la configuración.![][image13]	

## Nginx externo {#nginx-externo}

### Configuración {#configuración}

La instalación de Nginx será en la máquina de Ubuntu.

Nos conectamos a la máquina mediante SSH. ![][image14]

Y para instalarlo usaremos el comando apt install

### 

![][image15]

Para demostrar que el orden de los factores no altera el producto aquí usaremos el enabled antes que el start, pues el enable solo afecta al arranque y el start al uso actual.

Ahora si hacemos un status veremos como el servidor está encendido. ![][image16]

Para ahora que todo el mundo pueda acceder habilitamos en las reglas de entrada el puerto 80\.

![][image17]

Podemos ver como ya están abiertos puertos como el 443 para el https y otros puertos para otros servicios.

Al ser un servidor que sirve a la red le decimos que escuche para todas las ip y en cualquier red. 

Al buscar nuestra ip nos toparemos con la página predeterminada. 

Editamos el fichero de configuración de Nginx del virtual host sin TLS.

### HTTPS {#https-1}

Voy a instalar nano en red hat para editar

![][image18]

Creamos un directorio /etc/nginx/ssl

![][image19]

Para obtener un certificado oficial usamos un proveedor de certificados SSL como Let’s Encrypt.

Para Let’s Encrypt instalamos el cliente certbot y configuramos automaticamente SSL

![][image20]

Configuración de Nginx para HTTPS

El el archivo /etc/nginx/nginx.conf editamos el bloque server para https.

![][image21]

Al usar un certificado oficial como Let’s Encrypt ajustamos las rutas

![][image22]

También redirigimos HTTP a HTTPS

![][image23]

Guardamos y reiniciamos Nginx


