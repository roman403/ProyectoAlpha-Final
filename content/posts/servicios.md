---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "SERVICIOS"
---

## Nginx interno {#nginx-interno}

### Configuración

La instalación de Nginx será en la máquina de REDHAT.

Nos conectamos a la máquina mediante SSH. Y luego mediante el agent ssh entramos en la maquina redhat al no poder conectarnos directamente. Lo primero que hare sera instalar el nginx.

![](https://roman403.github.io/ProyectoAlpha-Final/ImagenNGX4.png)


Ahora deberemos cambiar la configuración de SELinux a 0 para poder evitar cualquier fallo.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX5.png)

Enviamos los documentos html con el comando scp.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX6.png)

Ahora iremos al fichero de configuración de nginx.

En el configuraremos también varios usuarios, siendo los 5 integrantes del grupo (en verdad deberían de ser miembros del departamento de informática).

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX7.png)

Para poder usar el html tendremos que descargar la herramienta zip, esto es debido a que redhat no la tiene por defecto.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX8.png)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX9.png)

Ahora hay que crear la carpeta donde estarán nuestros html.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX10.png)

Para que todo funcione ahora deberemos activar de manera por defecto nginx.

Ahora en caso de que se apague el servidor nginx se iniciará sin tener que usar el start.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX11.png)

Para acceder tendremos que primero conectarnos por vpn. Las reglas de entrada de AWS ya están cambiadas.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX12.png)

### HTTPS {#https}

Tenemos que crear un par de claves para añadirlo en la configuración.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX13.png)

Despues de crear el par de claves solo deberemos editar el fichero de configuración de nginx de redhat. Este par de claves al ser autofirmadas daran fallo.

![](https://roman403.github.io/ProyectoAlpha-Final/1.png)

## Nginx externo {#nginx-externo}

### Configuración {#configuración}

La instalación de Nginx será en la máquina de Ubuntu.

Nos conectamos a la máquina mediante SSH.

 ![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX14.png)

Y para instalarlo usaremos el comando apt install

### 

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX15.png)

Para demostrar que el orden de los factores no altera el producto aquí usaremos el enabled antes que el start, pues el enable solo afecta al arranque y el start al uso actual.

Ahora si hacemos un status veremos como el servidor está encendido.

 ![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX16.png)

Para ahora que todo el mundo pueda acceder habilitamos en las reglas de entrada el puerto 80\.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX17.png)

Podemos ver como ya están abiertos puertos como el 443 para el https y otros puertos para otros servicios.

Al ser un servidor que sirve a la red le decimos que escuche para todas las ip y en cualquier red. 

Al buscar nuestra ip nos toparemos con la página predeterminada. 

Editamos el fichero de configuración de Nginx del virtual host sin TLS.

### HTTPS {#https-1}

Voy a instalar nano en red hat para editar

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX18.png)

Creamos un directorio /etc/nginx/ssl

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX19.png)

Para obtener un certificado oficial usamos un proveedor de certificados SSL como Let’s Encrypt.

Para Let’s Encrypt instalamos el cliente certbot y configuramos automaticamente SSL

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX20.png)

Configuración de Nginx para HTTPS

El el archivo /etc/nginx/nginx.conf editamos el bloque server para https.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX21.png)

Al usar un certificado oficial como Let’s Encrypt ajustamos las rutas

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX22.png)

También redirigimos HTTP a HTTPS

![](https://roman403.github.io/ProyectoAlpha-Final/imagenNGX23.png)

Nota aqui el nombre no es darkkingdragon.com, es ventas.darkkingdragon.com.

Para obtener un certificado oficial usamos un proveedor de certificados SSL como Let’s Encrypt.

Para Let’s Encrypt instalamos el cliente certbot y configuramos automaticamente SSL

![](https://roman403.github.io/ProyectoAlpha-Final/2.png)

Guardamos y reiniciamos Nginx

![](https://roman403.github.io/ProyectoAlpha-Final/3.png)

