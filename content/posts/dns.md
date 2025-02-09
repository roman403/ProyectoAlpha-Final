---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "DNS"
---


Primer paso crear las máquinas en AWS y con la contraseña generada nos conectamos usando el acceso remoto de Windows poniendo de usuario Administrator y la ip pública de la máquina

 

Se ha usado Windows Server 2022

![](https://roman403.github.io/ProyectoAlpha-Final/dn1.png)

 
 Una vez nos hemos conectado, hay que instalar el DNS en roles y características


 ![](https://roman403.github.io/ProyectoAlpha-Final/dn2.png)


Nos metemos en herramientas administrativas y dns


 ![](https://roman403.github.io/ProyectoAlpha-Final/dn3.png)


 Creamos una zona nueva primaria


![](https://roman403.github.io/ProyectoAlpha-Final/dn4.png)


Con este dominio


![](https://roman403.github.io/ProyectoAlpha-Final/dn5.png)


Creo los registros que serán las máquinas que usaremos en el reto configuración directa


![](https://roman403.github.io/ProyectoAlpha-Final/dn6.png)


Configuración para la resolución inversa 


![](https://roman403.github.io/ProyectoAlpha-Final/dn7.png)


Para la transferencia al secundario que resuelva de manera inversa, añado la ip del ubuntu

solo le hará la transferencia a ese equipo para más seguridad que será el Ubuntu24


![](https://roman403.github.io/ProyectoAlpha-Final/dn8.png)


Cambio el dns de la máquina primaria y realizó una comprobación

Resolución inversa


![](https://roman403.github.io/ProyectoAlpha-Final/dn9.png)


Resolución directa


![](https://roman403.github.io/ProyectoAlpha-Final/dn10.png)


**Configuración máquina DNS secundaria Ubuntu** 

Nos conectamos a la máquina secundaria será un ubuntu 

Cambiamos el dns y ponemos la ip del primario

Instalamos el dns 

Configuración del ubuntu


![](https://roman403.github.io/ProyectoAlpha-Final/dn11.png)


Comprobación del funcionamiento de la resolución en el DNS secundario

Resolución Directa


![](https://roman403.github.io/ProyectoAlpha-Final/dn12.png)

Resolución Inversa


![](https://roman403.github.io/ProyectoAlpha-Final/dn13.png)