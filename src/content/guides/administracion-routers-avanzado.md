---
title: "Administración Avanzada de Routers"
description: "Aprende a configurar IPs, ocultar redes, filtrar por MAC y gestionar subredes WAN/LAN."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["router", "redes", "seguridad", "it-support"]
---

## Configuración Básica de IP
Todos los routers traen una IP de fábrica (ej: `192.168.1.1`). Cambiarla es vital por seguridad:
1. Accede al panel web (usualmente `admin / admin`).
2. Ve a la sección **LAN Setup**.
3. Cambia la IP a una subred diferente (ej: `10.0.0.1`). Esto evita conflictos con routers ISP.

---

## Seguridad: Red Invisible y Filtrado MAC
Para proteger una red de intrusos:

- <span class="protocol-tag protocol-ip">SSID</span> **Ocultar el SSID (Red Invisible)**: Desactiva la opción SSID Broadcast.
- <span class="protocol-tag protocol-udp">MAC ACL</span> **Filtrado por MAC**: Agrega las MACs de tus dispositivos permitidos.

---

## Configuración WAN/LAN (Subredes)
Si quieres que tu router reciba internet por una IP (WAN) y reparta por otra (LAN):
- **WAN**: Configúralo en modo "IP Estática" o "PPPoE" según tu proveedor.
- **LAN**: Define un pool de IPs diferente (ej: WAN recibe en `192.168.1.x` y LAN reparte en `172.16.x.x`).
- Esto crea un firewall natural entre tu red interna y la del proveedor.

---

## Clonación de Drivers
Si vas a reinstalar Windows y no tienes los drivers del fabricante:
Usa el comando de PowerShell (Admin):
```powershell
Export-WindowsDriver -Online -Destination C:\DriversBackup
```
Esto copiará todos los controladores de hardware actuales (incluyendo el del Router/Wifi) a una carpeta para usarlos luego.
