---
date : 2025-02-09T16:58:45+01:00
draft : false
title : "Backup"
---

## BACKUP

Para hacer backup de las máquinas que tenemos instaladas en AWS, podemos utilizar el servicio AWS Backup.

![][image62]

Iniciamos sesión en tu cuenta de AWS y abrimos la consola de administración.

Seleccionamos "Servicios" en la barra superior y escribimos "AWS Backup" en la barra de búsqueda.

Hacemos clic en "Crear plan de copia de seguridad".

![][image63]

Configuramos el plan de backup según nuestras necesidades, como la frecuencia de las copias de seguridad y la retención de datos. En nuestro caso haremos backup de todas las máquinas

![][image64]![][image65]

La copia la haremos semanalmente, los sábados a las 00:30

![][image66]

La copia de seguridad la podemos alojar dónde queramos, en este caso en Madrid

![][image67]

Pulsamos en crear plan.

Seleccionamos las máquinas o recursos que deseamos incluir en el plan de backup. En este caso todas las instancias

Elegiremos un rol IAM

![][image68]

Asignamos recursos

![][image69]

Guardamos el plan y nos aseguramos de que esté activado

![][image70]![][image71]![][image72]
