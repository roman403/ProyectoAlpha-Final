---
date : 2025-02-09T16:24:52+01:00
draft : false
title : "Wordpress"
---


### Instalacion {#instalacion}

Para su instalacion deberemos instalar un servidor mariadb y el php (seria lo suyo tener tambien el paquete de php-pfm)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd1.png)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd2.png)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd3.png)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd4.png)

Ahora deberemos poner tanto el php-fpm y el mariadb tanto enabled cómo iniciarlos.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd5.png)

Ahora en mariadb deberemos crear una base de datos y un usuario para poder hacer que wordpress funcione.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd6.png)

Ahora wordpress cuenta con un usuario para poder conectarse y realizar sus funciones, ahora vamos a configurar nginx para que pueda servir la pagina php de wordpress.

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd7.png)

![](https://roman403.github.io/ProyectoAlpha-Final/imagenwd8.png)