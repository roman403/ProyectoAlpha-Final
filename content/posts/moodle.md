---
date : 2025-02-09T16:58:45+01:00
draft : false
title : "MOODLE"
---

Vamos a instalar una herramienta en la instancia de Nginx/moodle. Para ello nos conectamos a ella a través de la instancia externa. En esta instancia ya tenemos instalado Mariadb, PHP, y Apache.

Creamos una base de datos para Moodle

Accedemos a Mariadb y creamos la base de datos llamada moodle, un usuario y le damos privilegios.

![](https://roman403.github.io/ProyectoAlpha-Final/M1.png)

Descargamos y configuramos Moodle en la carpeta /var/www/html
sudo yum install -y git 

![](https://roman403.github.io/ProyectoAlpha-Final/M2.png)


sudo git clone -b MOODLE_401_STABLE https://github.com/moodle/moodle.git 

![](https://roman403.github.io/ProyectoAlpha-Final/M3.png)

sudo mv moodle /var/www/html/moodle

![](https://roman403.github.io/ProyectoAlpha-Final/M4.png)

![](https://roman403.github.io/ProyectoAlpha-Final/M5.png)


Configuramos los permisos
sudo mkdir -p /var/www/moodledata 
sudo chown -R nginx:nginx /var/www/html/moodle /var/www/moodledata
sudo chmod -R 755 /var/www/html/moodle 
sudo chmod -R 777 /var/www/moodledata

![](https://roman403.github.io/ProyectoAlpha-Final/M6.png)


![](https://roman403.github.io/ProyectoAlpha-Final/M7.png)


Configuramos Nginx
Editamos el archivo de configuración de Nginx
sudo nano /etc/nginx/conf.d/moodle.conf


![](https://roman403.github.io/ProyectoAlpha-Final/M8.png)




Reiniciamos Nginx
sudo systemctl restart nginx

![](https://roman403.github.io/ProyectoAlpha-Final/M9.png)

Para configurar la base de datos en moodle entramos vía web a través del VPN
http://darkkingdragon.com/moodle
