---
title: "Redes Físicas: Cableado, Ponchado y Protocolos"
description: "Todo lo que necesitas saber sobre categorías de cable UTP, estándares de ponchado y protocolos de comunicación."
publishDate: 2024-03-22
author: "DanijDev"
tags: ["redes", "utp", "it-support", "infraestructura"]
---

## Introducción al Cableado Estructurado
El éxito de una red depende de la calidad física de sus conexiones. El cable UTP (Unshielded Twisted Pair) es el estándar de la industria.

### Categorías de Cable UTP
Existen varias categorías según su capacidad de transmisión:
- **Cat 5e**: Hasta 1 Gbps (100 MHz). Uso doméstico básico.
- **Cat 6**: Hasta 1 Gbps garantizado (250 MHz). Ideal para oficinas.
- **Cat 6a**: Hasta 10 Gbps (500 MHz). Uso profesional y servidores.
- **Cat 7/8**: Altas velocidades y blindaje extremo.

---

### Ponchado de Cables (Estándares)
Para ponchar un conector RJ45 se usan dos normas principales (TIA/EIA-568):

#### Norma A (T568A)
Es el estándar usado principalmente en instalaciones antiguas o cables cruzados.
<div class="wire-sequence">
    <div class="wire wire-w-green">1</div>
    <div class="wire wire-green">2</div>
    <div class="wire wire-w-orange">3</div>
    <div class="wire wire-blue">4</div>
    <div class="wire wire-w-blue">5</div>
    <div class="wire wire-orange">6</div>
    <div class="wire wire-w-brown">7</div>
    <div class="wire wire-brown">8</div>
</div>

#### Norma B (T568B)
Es el estándar más común en la actualidad para redes Ethernet.
<div class="wire-sequence">
    <div class="wire wire-w-orange">1</div>
    <div class="wire wire-orange">2</div>
    <div class="wire wire-w-green">3</div>
    <div class="wire wire-blue">4</div>
    <div class="wire wire-w-blue">5</div>
    <div class="wire wire-green">6</div>
    <div class="wire wire-w-brown">7</div>
    <div class="wire wire-brown">8</div>
</div>

### ¿Qué es un Cable Cruzado (Crossover)?
Un cable cruzado tiene un extremo en **Norma A** y el otro en **Norma B**. Se usa para conectar dos equipos iguales directamente (PC a PC o Switch a Switch) sin pasar por un router. *Nota: Hoy en día, la mayoría de tarjetas de red modernas lo hacen automáticamente (Auto MDI-X).*

---

## Protocolos de Red Esenciales
Los protocolos son las "reglas" de comunicación que permiten que los dispositivos se entiendan:

- <span class="protocol-tag protocol-ip">IP</span> **IP (Internet Protocol)**: Asigna direcciones únicas a cada equipo en la red.
- <span class="protocol-tag protocol-tcp">TCP</span> **TCP**: Protocolo orientado a conexión que garantiza que los datos lleguen completos.
- <span class="protocol-tag protocol-udp">UDP</span> **UDP**: Protocolo rápido para streaming o juegos, no garantiza el orden.
- <span class="protocol-tag protocol-dhcp">DHCP</span> **DHCP**: Servidor que asigna IPs automáticas para evitar conflictos.

---

## Tip de Pro
Al ponchar, asegúrate de que el forro del cable entre dentro del conector RJ45 antes de apretar con la ponchadora. Esto evita que los hilos se suelten con el movimiento y garantiza la durabilidad del cable.
