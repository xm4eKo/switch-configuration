---
title: NTP
sidebar_position: 4
---

# NTP (Network Time Protocol)

✅ **NTP (Network Time Protocol)** es un **protocolo de capa de aplicación** diseñado para **sincronizar los relojes de los dispositivos de una red** con una fuente de tiempo precisa. Está definido en **RFC 5905**.

---

## 👉 ¿Para qué sirve NTP?

- Garantiza que todos los dispositivos de una red (servidores, switches, routers, PCs) **tengan la hora exacta y uniforme**.
- Es esencial para tareas como:
  - Registros de logs coherentes.
  - Autenticación basada en tiempo (ejemplo: Kerberos).
  - Procesos financieros y transacciones electrónicas.

---

## 🛠️ ¿Cómo funciona NTP?

- Los dispositivos clientes se comunican con **servidores NTP** para obtener la hora actual.
- El protocolo **ajusta la hora local** tomando en cuenta:
  - La diferencia entre el reloj local y el servidor.
  - El **retardo de red (latencia)** para minimizar el error.
- Utiliza algoritmos que permiten **compensar pequeñas desviaciones (drift)** de los relojes.

---

## 🏗️ Estructura jerárquica (niveles de estrato):

NTP organiza las fuentes de tiempo en **estratos (stratum)**:

- **Stratum 0**: Fuentes de tiempo de referencia muy precisas (relojes atómicos, GPS).
- **Stratum 1**: Servidores conectados directamente a stratum 0.
- **Stratum 2**: Servidores que se sincronizan con stratum 1.
- …y así sucesivamente.

Cuanto más alto el número de estrato, **más lejos está de la fuente primaria de tiempo**, aunque sigue manteniendo una precisión aceptable.

---

## 🎯 Características importantes de NTP:

✅ Puede sincronizar con una precisión de **milisegundos en redes LAN** y de **decenas de milisegundos en Internet pública**.
✅ Funciona sobre **UDP**, **puerto 123**.
✅ Incluye mecanismos de seguridad opcionales (como autenticación basada en claves).

---

## 🚩 Consideraciones:

- Es común configurar múltiples servidores NTP para mayor confiabilidad y evitar dependencias de un solo punto.
- Algunos dispositivos usan versiones más simples como **SNTP (Simple Network Time Protocol)**, menos precisa pero más ligera.

:::tip Dato Adicional
Muchos sistemas operativos (Windows, Linux, macOS) tienen clientes NTP integrados que se configuran automáticamente o manualmente para sincronizar la hora.
:::
