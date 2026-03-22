---
title: "Cómo instalar o actualizar Android: Guía de Flasheo"
description: "Guía definitiva para cambiar el sistema operativo de tu Android (Update/Downgrade/Custom ROM)."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["flashing", "android", "rom", "update"]
---

## Introducción al Flasheo de Android
Instalar un sistema desde cero (Flashear) es necesario cuando el software está dañado, quieres actualizar manualmente o deseas instalar una Custom ROM.

### Requisitos Previos
1. **Drivers**: Instala los drivers de tu marca (Samsung, Xiaomi, Qualcomm).
2. **Cable USB**: Usa preferiblemente el original.
3. **Batería**: Mínimo 50% de carga.

---

## Paso 1: Identificar el Software Correcto
Nunca instales un software de un modelo distinto. Verifica tu modelo exacto en:
`Ajustes > Acerca del teléfono > Modelo` o usando el comando `adb shell getprop ro.product.model`.

## Paso 2: El proceso por Marca
- **Samsung**: Usa la herramienta **Odin**. Carga los 4 archivos (BL, AP, CP, CSC) y pon el celular en modo *Download*.
- **Xiaomi**: Usa **MiFlash Tool**. Requiere que el Bootloader esté desbloqueado. Se flashea en modo *Fastboot*.
- **Motorola**: Se realiza usualmente por consola usando comandos `fastboot flash partition`.

## Advertencia Técnica
El flasheo borra todos los datos del equipo. Asegúrate de tener una copia de seguridad y el desbloqueo de OEM activo si es necesario.

> **Tip de Experto**: Si el equipo se queda en el logo después de flashear, realiza un "Wipe Data" desde el modo Recovery.
