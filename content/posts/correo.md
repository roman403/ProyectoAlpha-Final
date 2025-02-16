---
date : 2025-02-09T16:58:45+01:00
draft : false
title : "CORREO"
---

Empezamos instalando postfix

sudo apt-get update
sudo apt-get install postfix

Nombre de sistema de correo ponemos nuestro dominio 

selecionamos sitio de internet

Archivo de configuracion de postfix
![](https://roman403.github.io/ProyectoAlpha-Final/MAINCF.jpeg)

creamos lo usuarios 

sudo adduser cliente1
sudo adduser cliente2

Para mandar un correo de un usuario a otro usuario usamos:
desde el clinte1
mail client2@darkkingdragon.com

![](https://roman403.github.io/ProyectoAlpha-Final/cliente1envia.jfif)

Para comprobar que lo ha recibido el cliente2 nos loegamos como el y lo comprobamos

![](https://roman403.github.io/ProyectoAlpha-Final/cliente2Recibe.jfif)

sudo apt update
sudo apt install dovecot-imapd dovecot-pop3d

Configuracion

![](https://roman403.github.io/ProyectoAlpha-Final/mail.conf.jfif)