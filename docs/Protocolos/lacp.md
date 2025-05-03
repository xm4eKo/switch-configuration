---
title: LACP
sidebar_position: 2
---

# LACP (Link Aggregation Control Protocol)

✅ **LACP (Link Aggregation Control Protocol)** es un protocolo de la capa 2 (enlace de datos), definido por el estándar **IEEE 802.3ad (ahora parte de 802.1AX)**. Su objetivo principal es **agrupar varios enlaces físicos (cables de red) en un único enlace lógico** para aumentar el ancho de banda y mejorar la redundancia.

---

## 👉 ¿Qué hace LACP?

- Permite que **varios puertos Ethernet trabajen juntos como si fueran uno solo** (un "link aggregation group" o **LAG**).
- Si un cable falla, el tráfico se redirige automáticamente por los enlaces restantes, evitando la pérdida de conexión **(tolerancia a fallos)**.
- Combina el ancho de banda de todos los enlaces para mejorar la velocidad total disponible.

---

## 🛠️ ¿Cómo funciona?

- Los dispositivos (por ejemplo, dos switches o un switch y un servidor) intercambian **paquetes LACPDU (LACP Data Units)** para negociar y acordar qué enlaces se unirán al grupo.
- LACP decide automáticamente qué enlaces son válidos y activos dentro del grupo.
- Si un puerto agregado falla o se desconecta, LACP lo saca automáticamente del grupo sin afectar los demás.

---

## 🎯 Beneficios principales:

✅ **Mayor ancho de banda**: suma las velocidades de los enlaces (ejemplo: 2 puertos de 1 Gbps = 2 Gbps agregados).
✅ **Alta disponibilidad**: si un enlace falla, el tráfico sigue funcionando por los demás.
✅ **Balanceo de carga**: distribuye el tráfico entre los enlaces (según MAC, IP, o número de puerto, dependiendo de la configuración).

---

## 🚩 Requisitos importantes:

- Los enlaces deben tener las mismas características (velocidad, dúplex, etc.).
- Deben conectarse entre dispositivos compatibles con LACP.
- Normalmente se usa en **switches**, **servidores**, **routers** y **firewalls de nivel empresarial**.

:::tip Dato Adicional
Si no usas LACP, puedes configurar agregación de enlaces de forma estática (sin protocolo de negociación), pero pierdes la capacidad de detección automática de fallos.
:::
