---
title: "Diagnóstico: Mi PC no enciende o no da video"
description: "Guía paso a paso para identificar fallas de hardware en computadoras de escritorio y laptops."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["hardware", "reparacion", "it-support", "diagnostico"]
---

## Introducción al Diagnóstico de Hardware
Cuando un equipo no enciende o se queda en pantalla negra, el técnico debe seguir un protocolo de descarte lógico para evitar gastos innecesarios.

### Paso 1: Verificación de Energía
Antes de abrir el equipo, descarta lo externo:
- **Cables**: Prueba con un cable de poder diferente.
- **Fuentes de Laptop**: Mide el voltaje del cargador con un multímetro. Debe coincidir con la etiqueta (ej: 19V).
- **Botón de Encendido**: Si es desktop, puentea los pines `PWR_SW` en la placa madre para descartar fallo del botón del case.

---

## Paso 2: El Proceso de Descarte (POST)
Si el equipo prende luces pero no da imagen, el problema suele estar en:

1. **Memoria RAM**: 
   - Limpia los contactos de la RAM con un borrador de nata.
   - Prueba los módulos uno por uno en diferentes ranuras.
2. **BIOS / Pila CMOS**: 
   - Retira la pila CR2032 por 30 segundos para resetear la BIOS (Clear CMOS).
3. **Tarjeta de Video**: 
   - Si tienes procesador con gráficos integrados, conecta el monitor directamente a la placa base.

---

## Paso 3: Fallas de Placa o Procesador
Si tras limpiar RAM y resetear BIOS no hay video:
- **Prueba de Mínimos**: Desconecta discos duros, lectores y periféricos. Deja solo Placa, Procesador y 1 RAM.
- **Inspección Visual**: Busca capacitores inflados o rastros de quemaduras en la zona de los VRM.

> **Consejo Pro**: Escucha los pitidos (Beep Codes). Un pitido largo y dos cortos suelen indicar error de video; pitidos constantes suelen ser memoria RAM.
