---
title: STP
sidebar_position: 6
---

# STP (Spanning Tree Protocol)

✅ **STP (Spanning Tree Protocol)** es un **protocolo de capa 2 (enlace de datos)**, definido por **IEEE 802.1D**, cuyo objetivo principal es **evitar bucles de red en redes conmutadas (switching)**.

En una red de switches, los bucles pueden ocurrir fácilmente si hay caminos redundantes. Estos bucles causan que los frames se repliquen infinitamente, **colapsando la red**. STP previene esto **bloqueando enlaces redundantes de forma automática**, manteniendo solo un camino activo entre dos dispositivos.

---

## 👉 ¿Qué hace STP?

- Detecta **topologías redundantes**.
- Desactiva (bloquea) automáticamente ciertos puertos para eliminar bucles lógicos.
- Si el camino activo falla, **reactiva automáticamente** uno de los caminos bloqueados para mantener la conectividad.

---

## 🛠️ ¿Cómo funciona STP?

1. **Elección de un Root Bridge (switch raíz)**: Todos los switches eligen al switch con el **Bridge ID más bajo** como raíz.
2. Cada switch calcula el **camino más corto hacia el Root Bridge**.
3. Se asignan roles a los puertos:
   - **Root Port (RP)**: puerto con el mejor camino al Root Bridge.
   - **Designated Port (DP)**: puerto que representa el camino más óptimo hacia una red.
   - **Blocked Port**: puerto que se bloquea para evitar bucles.
4. Se utilizan mensajes **BPDUs (Bridge Protocol Data Units)** para intercambiar información de topología entre switches.

---

## 🎯 Beneficios de STP:

✅ Evita **bucles de broadcast** que podrían saturar la red.

✅ Permite tener **caminos redundantes sin riesgo de bucles**, mejorando la disponibilidad.

✅ Reconfigura automáticamente la topología si un enlace o switch falla.

---

## 🚩 Limitaciones de STP:

- C**onvergencia lenta**: tarda entre 30-50 segundos en reaccionar ante un cambio de topología (dependiendo de la implementación).
- No prioriza balanceo de carga: solo un camino está activo, los otros están inactivos (bloqueados).

Por eso existen **versiones mejoradas de STP**, como:

- **RSTP (Rapid Spanning Tree Protocol, IEEE 802.1w)**: más rápido.
- **MSTP (Multiple Spanning Tree Protocol, IEEE 802.1s)**: permite manejar múltiples instancias de STP para diferentes VLANs.

---

## 📌 Ejemplo práctico:

Supón 3 switches conectados en un triángulo. Si no existiera STP, un broadcast podría circular indefinidamente entre ellos. Con STP, uno de los enlaces será bloqueado, eliminando el bucle y manteniendo un solo camino lógico.

:::tip Dato Adicional
Aunque STP evita bucles, si se configura incorrectamente o se desactiva en algún switch, los bucles pueden volver a aparecer.
:::
