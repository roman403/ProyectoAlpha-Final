---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "VPN"
---

## OpenVPN {#openvpn}

Tenemos que instalar el servicio de openVPN.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen32.png)

Ahora deberemos de instalar easy-RSA para poder gestionar el tema de usuarios

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen33.png)

Despues de instalarlo creamos una carpeta para poder gestionarlo.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen34.png)

Ahora deberemos añadir esta ruta como symlink para que pueda acceder facilmente la aplicacion de easy-RSA.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen35.png)

Ahora deberemos crear una PKI en el home de easy-rsa.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen36.png)

Ejecutamos el comando easyrsa.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen37.png)

Ahora tomara la configuración que creamos antes. Ahora le daremos un nombre a la maquina para poder acceder, además crea las claves privada y publica.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen38.png)

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen39.png)

Ahora deberemos de mover la clave a el directorio de openvpn.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen40.png)

Ahora cogemos la configuración de ejemplo y la pasamos al fichero de openvpn.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen41.png)

Ahora vamos al fichero de configuración.

![](https://roman403.github.io/ProyectoAlpha-Final/Imagen42.png)

Uso esta guía. [https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-ubuntu-20-04-es](https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-ubuntu-20-04-es)