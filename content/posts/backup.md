---
date : 2025-02-09T16:58:45+01:00
draft : false
title : "Backup"
---


Para hacer backup de las máquinas que tenemos instaladas en AWS, podemos utilizar el servicio AWS Backup.

![](https://roman403.github.io/ProyectoAlpha-Final/backup1.png)

Iniciamos sesión en tu cuenta de AWS y abrimos la consola de administración.

Seleccionamos "Servicios" en la barra superior y escribimos "AWS Backup" en la barra de búsqueda.

Hacemos clic en "Crear plan de copia de seguridad".

![](https://roman403.github.io/ProyectoAlpha-Final/backup2.png)

Configuramos el plan de backup según nuestras necesidades, como la frecuencia de las copias de seguridad y la retención de datos. En nuestro caso haremos backup de todas las máquinas

![](https://roman403.github.io/ProyectoAlpha-Final/backup3.png)



![](https://roman403.github.io/ProyectoAlpha-Final/backup4.png)

La copia la haremos semanalmente, los sábados a las 00:30

![](https://roman403.github.io/ProyectoAlpha-Final/backup5.png)

La copia de seguridad la podemos alojar dónde queramos, en este caso en Madrid

![](https://roman403.github.io/ProyectoAlpha-Final/backup6.png)

Pulsamos en crear plan.

Seleccionamos las máquinas o recursos que deseamos incluir en el plan de backup. En este caso todas las instancias

Elegiremos un rol IAM

![](https://roman403.github.io/ProyectoAlpha-Final/backup7.png)

Asignamos recursos

![](https://roman403.github.io/ProyectoAlpha-Final/backup8.png)

Guardamos el plan y nos aseguramos de que esté activado

![](https://roman403.github.io/ProyectoAlpha-Final/backup9.png)

![](https://roman403.github.io/ProyectoAlpha-Final/backup10.png)

![](https://roman403.github.io/ProyectoAlpha-Final/backup11.png)
