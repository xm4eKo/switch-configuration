---
title: BPDU
sidebar_position: 7
---

# BPDU (Bridge Protocol Data Unit)

✅ **BPDU (Bridge Protocol Data Unit)** es un tipo de mensaje utilizado por el protocolo **STP (Spanning Tree Protocol)**, que opera en la **capa 2 (enlace de datos)**. Su función es **intercambiar información entre switches para evitar bucles en la red Ethernet**.

---

## 👉 ¿Qué hace una BPDU?

- Permite que los switches **compartan información sobre la topología de la red** para decidir qué puertos deben estar activos y cuáles bloqueados, evitando **loops (bucles)** que causarían tormentas de broadcast.
- Mediante el intercambio de BPDUs, los switches eligen un **root bridge (switch raíz)** y configuran el estado de cada puerto (root port, designated port, blocked port).

---

## 🛠️ Tipos de BPDUs:

1. **Configuration BPDU (CBPDU)**: se usa para construir y mantener el árbol de expansión (STP).
2. **Topology Change Notification BPDU (TCN BPDU)**: informa a la red de que hubo un cambio en la topología (por ejemplo, un puerto que pasó de down a up).

---

## 🎯 ¿Por qué son importantes las BPDUs?

✅ Ayudan a **prevenir bucles de capa 2**, que pueden colapsar una red.

✅ Permiten que la red **se adapte automáticamente** a cambios (si un cable o switch falla, se puede reconfigurar).

✅ Usadas por protocolos como **STP**, **RSTP (Rapid Spanning Tree Protocol)**, **y MSTP (Multiple Spanning Tree Protocol)**.

---

## 🚩 Riesgos y seguridad:

- Si un atacante envía **BPDUs maliciosas**, puede forzar al switch a elegir un nuevo root bridge, causando interrupciones **(ataque BPDU spoofing)**.
- Para proteger la red, se usan mecanismos como **BPDU Guard** o **Root Guard** en los switches.

:::tip Dato Adicional
Las BPDUs se envían a la **dirección MAC de multicast 01:80:C2:00:00:00**, reservada para protocolos de puenteo.
:::
