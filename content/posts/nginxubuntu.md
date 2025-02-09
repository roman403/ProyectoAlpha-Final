---
date : 2025-02-09T17:08:25+01:00
draft : false
title : "Nginxubuntu"
---

Instalación de Nginx: Nos conectamos a la instancia y descargamos Nginx, previamente actualizamos

![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu1.png)

![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu2.png)

### **Verificamos la instalación**

Para asegurarnos de que NGINX está instalado correctamente, revisamos su estado:

sudo systemctl status nginx

Si NGINX no está activo, lo iniciamos manualmente:

sudo systemctl start nginx

Y para asegurarnos de que se inicie automáticamente el sistema:

sudo systemctl enable nginx

![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu3.png)

También verificamos que el **Grupo de Seguridad (Security Group)** de la instancia en AWS tiene las reglas correctas:

* **Puerto 80 (HTTP)** → Permitir tráfico entrante.  
* **Puerto 443 (HTTPS)** → Permitir tráfico entrante.

![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu4.png)

Habilitamos HTTPS con Let's Encrypt

sudo apt install certbot python3-certbot-nginx \-y 

sudo certbot \--nginx \-d darkkingdragon.com \-d [www.darkkingdragon.com](http://www.darkkingdragon.com)

![]![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu5.png)

![]![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu6.png)

Renovamos automáticamente el certificado

![]![](https://roman403.github.io/ProyectoAlpha-Final/nginxubuntu7.png)