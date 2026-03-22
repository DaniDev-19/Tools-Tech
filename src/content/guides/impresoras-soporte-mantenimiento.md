---
title: "Impresoras: Soporte, Tóner y Redes"
description: "Guía completa para instalar, mantener y solucionar fallas en impresoras de inyección y láser."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["impresoras", "soporte-tecnico", "hardware", "mantenimiento"]
---

## Instalación y Configuración
Hoy en día, la mayoría se instalan solas (Plug & Play), pero para empresas se recomienda:
1. **IP Estática**: Si es una impresora de red, asígnale una IP fija fuera del rango DHCP del Router.
2. **Drivers Universales**: Si el driver específico falla, los drivers "Universal Print Driver" de HP o Samsung suelen salvar el día.

---

## Mantenimiento: Tóner y Cartuchos
- <span class="protocol-tag protocol-ip">LÁSER</span> **Láser (Tóner)**: Si la impresión sale clara, agita el tóner.
- <span class="protocol-tag protocol-udp">INK</span> **Inyección (Tintas)**: Usa la utilidad "Limpieza de Cabezales".

### Fallas Comunes
- **Atascos de papel**: Nunca jales el papel con fuerza hacia atrás. Sigue siempre la ruta de salida del papel para no dañar los rodillos o el fusor.
- **Cola de impresión bloqueada**: Si los documentos no salen, ejecuta en consola:
```batch
net stop spooler
del /Q /F /S "%systemroot%\System32\Spool\Printers\*.*"
net start spooler
```

---

## Cómo compartir una Impresora en Red
Si la impresora es USB y quieres que otra PC la use:
1. En la PC conectada: Propiedades de la impresora > **Compartir**.
2. En la otra PC: `Panel de Control > Dispositivos e Impresoras > Agregar`.
3. Busca por nombre: `\\NombreDeLaPC\NombreDeLaImpresora`.

> **Nota**: Ambas PCs deben estar en el mismo Grupo de Trabajo y tener el descubrimiento de redes activado.
