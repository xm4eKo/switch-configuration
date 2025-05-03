---
title: LLDP
sidebar_position: 1
---

# LLDP (Link Layer Discovery Protocol)

✅ **LLDP (Link Layer Discovery Protocol)** es un **protocolo de descubrimiento de capa 2 (enlace de datos)** definido por el estándar **IEEE 802.1AB**. Su función principal es permitir que los dispositivos de red (como switches, routers, puntos de acceso, etc.) anuncien su identidad y capacidades a los dispositivos directamente conectados.

## 👉 ¿Qué hace?

- Permite que un dispositivo envíe periódicamente información sobre sí mismo (nombre,puerto,modelo,versión de firmware, VLAN, etc.) a los dispositivos vecinos.
- Estos dispositivos reciben y almacenan esa información, lo que ayuda a **mapear la topología de la red automáticamente** o a diagnosticar problemas.

## 🛠️ ¿Cómo funciona?

- La información se envía en mensajes llamados **LLDPDUs (LLDP Data Units)** dentro de tramas Ethernet específicas (con Ethertype 0x88cc).
- Los datos se organizan en **TLVs (Type-Length-Value)**, que contiene campos como:
  - **Chassis ID**: identifica el chasis del dispositivo.
  - **Port ID**: identifica el puerto que envía el mensaje.
  - **TTL (Time To Live)**: cuánto tiempo es válida la información.

## 🎯 Usos típicos de LLDP:

- Descubrir qué dispositivo está conectado a qué puerto (muy útil en redes grandes).
- Integración con sistemas de gestión de red (NMS).
- Configuración automática de teléfonos VoIP y otros dispositivos que soporten LLDP-MED (extensión para equipos multimedia).

:::tip Dato Adicional
LLDP es **vendor-neutral**, es decir, no depende de la marca del fabricante, a diferencia de CDP (Cisco Discovery Protocol), que es propietario de Cisco.
:::
