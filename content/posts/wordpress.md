---
date : 2025-02-09T16:24:52+01:00
draft : false
title : "Wordpress"
---

## Wordpress {#wordpress}

### Instalacion {#instalacion}

Para su instalacion deberemos instalar un servidor mariadb y el php (seria lo suyo tener tambien el paquete de php-pfm)

![][image24]

![][image25]

![][image26]

![][image27]

Ahora deberemos poner tanto el php-fpm y el mariadb tanto enabled cómo iniciarlos.

![][image28]

Ahora en mariadb deberemos crear una base de datos y un usuario para poder hacer que wordpress funcione.

![][image29]

Ahora wordpress cuenta con un usuario para poder conectarse y realizar sus funciones, ahora vamos a configurar nginx para que pueda servir la pagina php de wordpress.

![][image30]

![][image31]