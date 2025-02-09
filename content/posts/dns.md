---
date : 2025-02-09T12:19:03+01:00
draft : false
title : "Dns"
---

El servidor Dns primario es un Windows

# Configuración de DNS en AWS

## Paso 1: Crear las máquinas en AWS

Creamos las máquinas en AWS y usamos la contraseña generada para conectarnos mediante acceso remoto de Windows. Usamos el usuario `Administrator` y la IP pública de la máquina.

**Sistema Operativo:** Windows Server 2022

![a](https://roman403.github.io/ProyectoAlpha-Final/Grub01.jpg)



---

## Paso 2: Instalación del DNS

Una vez conectados, instalamos el servicio DNS desde **Roles y Características**.

![Instalación de DNS](https://roman403.github.io/ProyectoAlpha/dns2.png)

---

## Paso 3: Acceso a Herramientas Administrativas

Nos dirigimos a **Herramientas Administrativas** y seleccionamos **DNS**.

![Herramientas Administrativas - DNS](https://roman403.github.io/ProyectoAlpha/dns3.png)

---

## Paso 4: Crear una zona primaria

Creamos una **Zona Nueva Primaria**.

![Crear zona primaria](https://roman403.github.io/ProyectoAlpha/dns4.png)

---

## Paso 5: Configurar el dominio

Configuramos el dominio deseado.

![Configuración del dominio](https://roman403.github.io/ProyectoAlpha/dns5.png)

---

## Paso 6: Crear alias para las máquinas

Creamos 4 alias que representarán las máquinas que usaremos en el reto (utilizando las IPs privadas).

![Crear alias](https://roman403.github.io/ProyectoAlpha/dns6.png)

---

## Paso 7: Configurar un servidor secundario

Añadimos un servidor secundario, configurado para realizar la transferencia solo a dicho equipo por motivos de seguridad. Este servidor será una máquina con **Ubuntu 24**.

![Configuración del servidor secundario](https://roman403.github.io/ProyectoAlpha/dns7.png)

---

## Paso 8: Cambiar el DNS de la máquina primaria y realizar comprobaciones

Modificamos la configuración del DNS en la máquina primaria y realizamos una comprobación para validar los cambios.

![Cambio y comprobación del DNS](https://roman403.github.io/ProyectoAlpha/dns8.png)

---

## Paso 9: Configuración del servidor secundario

1. Nos conectamos a la máquina secundaria, que será un servidor con **Ubuntu 24**.
2. Cambiamos la configuración del DNS, apuntando a la IP de la máquina primaria.
3. Instalamos el servicio DNS en Ubuntu.