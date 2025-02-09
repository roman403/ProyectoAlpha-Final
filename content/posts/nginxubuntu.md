---
date : 2025-02-09T17:08:25+01:00
draft : false
title : "Nginxubuntu"
---

Instalación de Nginx: Nos conectamos a la instancia y descargamos Nginx, previamente actualizamos

![][image56]

### **Verificamos la instalación**

Para asegurarnos de que NGINX está instalado correctamente, revisamos su estado:

sudo systemctl status nginx

Si NGINX no está activo, lo iniciamos manualmente:

sudo systemctl start nginx

Y para asegurarnos de que se inicie automáticamente el sistema:

sudo systemctl enable nginx

![][image57]

También verificamos que el **Grupo de Seguridad (Security Group)** de la instancia en AWS tiene las reglas correctas:

* **Puerto 80 (HTTP)** → Permitir tráfico entrante.  
* **Puerto 443 (HTTPS)** → Permitir tráfico entrante.

![][image58]

Habilitamos HTTPS con Let's Encrypt

sudo apt install certbot python3-certbot-nginx \-y 

sudo certbot \--nginx \-d darkkingdragon.com \-d [www.darkkingdragon.com](http://www.darkkingdragon.com)

![][image59]

![][image60]

Renovamos automáticamente el certificado

![][image61]