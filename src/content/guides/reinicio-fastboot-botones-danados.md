---
title: "Reiniciar Xiaomi/Android con botones dañados"
description: "Aprende cómo entrar a Recovery o reiniciar tu equipo usando comandos Fastboot cuando los botones físicos no funcionan."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["xiaomi", "fastboot", "reparacion", "botones"]
---

## El problema de los botones dañados
Es muy común que en soporte técnico recibamos equipos con los botones de volumen o encendido inservibles. Si el equipo está en modo Fastboot (conejo de Xiaomi), parece imposible salir de ahí.

### Solución por Consola
La solución es conectar el equipo al PC y usar nuestra Consola ADB & Fastboot.

---

## Comandos de Rescate

### 1. Salir del modo "Conejo" (Xiaomi Fastboot)
Si el equipo se quedó pegado en el logo de Fastboot:
```bash
fastboot reboot
```
Esto obligará al sistema a iniciar normalmente.

### 2. Forzar el inicio a Recovery sin botones
Si necesitas formatear pero el botón Vol+ no sirve:
```bash
adb reboot recovery
```
*(Requiere que el sistema esté encendido y con depuración activa).*

### 3. Verificar si el equipo responde
Si no sabes si el cable o el puerto de carga sirven:
```bash
fastboot devices
```
Si aparece un código alfanumérico, el equipo está listo para recibir comandos.

---

## Tip para Técnicos
Si el botón de encendido está en corto (se presiona solo), el equipo entrará en un bucle de reinicio. En ese caso, la única solución es abrir el equipo y desconectar el flex de botones antes de intentar cualquier comando.
