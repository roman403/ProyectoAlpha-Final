---
date: 2025-02-09T12:15:37+01:00
draft: false
title: "Arquitectura"
---

Esta es la infraestructura usada en este proyecto

Se realizo en AWS con las siguientes máquinas

![](https://roman403.github.io/ProyectoAlpha-Final/infraestructura.jfif)

# Estructura de la red {#estructura-de-la-red}

![](https://roman403.github.io/ProyectoAlpha-Final/imagen1.png)
Esa será la estructura de nuestra red. Nos conectaremos a las maquinas sin ip flotante mediante el agente ssh.

![](https://roman403.github.io/ProyectoAlpha-Final/imagen2.png)

Tenemos dos máquinas que darán servicio en internet, serán un windows, permitiendo usar su resolución de nombres para nuestro dominio y un mail para que nuestros empleados y nuestros clientes puedan hacer uso de él. Y la otra maquina que dara servicio de un segundo DNS para evitar sobrecargar el primario, teniendo el todas las ip de la red interna para poder hacer buen uso, además contara con un nginx que dará servicio a nuestra página en internet. Ademas de eso tendremos un ubuntu que hace servicio de VPN

En nuestra red interna un redhat que tiene de servicios, wordpress, moodle y  nginx.



# S.O. {#s.o.}

Hemos elegido varios S.O. cada uno centrado en una tarea para un mejor rendimiento y una mayor redundancia. Así evitamos que si una maquina se cae sea lo que perjudique a varios servicios a la vez.


![](https://roman403.github.io/ProyectoAlpha-Final/imagen3.png)

# Red Hat Enterprise Linux 

En esta instancia tendremos el Moodel y Nginx interno


![](https://roman403.github.io/ProyectoAlpha-Final/redhat.png)


# Windows Server 2022

Esta instancia actuará de Dns primario 

![](https://roman403.github.io/ProyectoAlpha-Final/dnswindows.png)



# Linux/UNIX Ubuntu24 

Contiene el nginx externo, tambien actuará de Dns secundario 

![](https://roman403.github.io/ProyectoAlpha-Final/externanginx.png)


# Linux/UNIX Ubuntu 24

En está instacia está el sofware del OpenVpn

![](https://roman403.github.io/ProyectoAlpha-Final/vpnlinux.png)

