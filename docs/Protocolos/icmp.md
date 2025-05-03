---
title: ICMP
sidebar_position: 3
---

# ICMP (Internet Control Message Protocol)

✅ **ICMP (Internet Control Message Protocol)** es un **protocolo de la capa de red (capa 3)** definido en el estándar **RFC 792**. Su función principal es **enviar mensajes de control y diagnóstico entre dispositivos de red** para reportar errores o informar sobre el estado de la comunicación IP.

---

## 👉 ¿Qué hace ICMP?

- Permite que los dispositivos **notifiquen problemas en la entrega de paquetes IP**, como cuando un host es inalcanzable o una ruta no existe.
- También se usa para **probar la conectividad y el rendimiento de la red** (por ejemplo, con los comandos **ping** y **traceroute**).

---

## 🛠️ Ejemplos de mensajes ICMP más comunes:

| Tipo de mensaje         | Descripción                                                  |
| ----------------------- | ------------------------------------------------------------ |
| Echo Request            | Solicitud de prueba (usada por **ping**)                     |
| Echo Reply              | Respuesta a Echo Request                                     |
| Destination Unreachable | Indica que un destino no es alcanzable                       |
| Time Exceeded           | El TTL de un paquete llegó a cero (usado por **traceroute**) |
| Redirect                | Indica que hay una mejor ruta disponible                     |

---

## 🎯 Usos principales de ICMP:

✅ **Diagnóstico de red**: comprobar si un host responde (ping) o trazar la ruta de los paquetes (traceroute).
✅ **Notificación de errores**: informar de problemas en la entrega de paquetes sin interrumpir la comunicación de otros paquetes.
✅ **Control de flujo de red**: avisar si un host o router necesita cambiar su comportamiento (por ejemplo, mensajes Redirect).

---

## 🚩 Cosas a tener en cuenta:

- ICMP **no transporta datos de usuario**, solo mensajes de control.
- Puede ser **bloqueado por firewalls** o configuraciones de seguridad para evitar ataques como **ping flood** o **ICMP tunneling**.
- **No usa TCP ni UDP**, sino que viaja directamente sobre IP (protocolo número 1 en el campo "protocol" del encabezado IP).

:::info Dato Curioso
Aunque ICMP ayuda al diagnóstico, también ha sido usado en ataques de red (ejemplo: ICMP flood, Smurf attack), por lo que muchas redes restringen su uso.
:::
