---
title: "Gestión de Archivos y Usuarios en Red"
description: "Cómo administrar perfiles de usuario, compartir carpetas y respaldar datos entre PCs usando solo un cable."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["windows", "usuarios", "red-local", "respaldo"]
---

## Usuarios y Perfiles de Windows
Un técnico debe saber gestionar cuentas para varios empleados:
- **Cuentas Locales**: No requieren internet (Modo Pro). Crea una con `net user nombre contraseña /add`.
- **Perfiles dañados**: Si un perfil no carga, puedes crear uno nuevo y copiar la carpeta `C:\Users\Antiguo` a `C:\Users\Nuevo`.

---

## Compartir Carpetas en Red Local
- <span class="protocol-tag protocol-tcp">SMB/CIFS</span> **Protocolo de Compartición**: Usa el estándar de Windows para mover archivos en LAN.
1. Clic derecho en la carpeta > **Propiedades** > **Compartir**.
2. Dale permisos a "Todos" o a un usuario específico.
3. En las opciones de red del Panel de Control, desactiva el "Uso compartido con protección por contraseña" si quieres acceso rápido (solo en redes seguras).

---

## Respaldo PC a PC (Sin Internet)
Si tienes que pasar 200GB de una PC vieja a una nueva y no tienes un disco externo:
1. Conecta ambas PCs con un **cable de red** (Directo o Cruzado).
2. Asigna IPs estáticas (ej: PC1: `192.168.1.10` / PC2: `192.168.1.11`).
3. Comparte la carpeta contenedora en la PC vieja.
4. En la PC nueva, entra por `\\192.168.1.10` y comienza a copiar. *La velocidad será de hasta 1Gbps (125MB/s).*

---

## Limpieza de Temporales Eficiente
Para liberar espacio rápidamente sin programas:
Crea un archivo `.bat` con esto:
```batch
del /s /f /q %temp%\*.*
del /s /f /q C:\Windows\temp\*.*
powershell -command "Clear-RecycleBin -Force"
```
Ejecútalo como administrador cada semana para mantener el sistema ágil.
