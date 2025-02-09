---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "VPN"
---

## OpenVPN {#openvpn}

Tenemos que instalar el servicio de openVPN.

![][image32]

Ahora deberemos de instalar easy-RSA para poder gestionar el tema de usuarios

![][image33]

Despues de instalarlo creamos una carpeta para poder gestionarlo.

![][image34]

Ahora deberemos añadir esta ruta como symlink para que pueda acceder facilmente la aplicacion de easy-RSA.

![][image35]

Ahora deberemos crear una PKI en el home de easy-rsa.

![][image36]

Ejecutamos el comando easyrsa.

![][image37]

Ahora tomara la configuración que creamos antes. Ahora le daremos un nombre a la maquina para poder acceder, además crea las claves privada y publica.

![][image38]

![][image39]

Ahora deberemos de mover la clave a el directorio de openvpn.

![][image40]

Ahora cogemos la configuración de ejemplo y la pasamos al fichero de openvpn.

![][image41]

Ahora vamos al fichero de configuración.

![][image42]

Uso esta guía. [https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-ubuntu-20-04-es](https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-ubuntu-20-04-es)