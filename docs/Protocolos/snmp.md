---
title: SNMP
sidebar_position: 9
---

# SNMP (Simple Network Management Protocol)

✅ **SNMP (Simple Network Management Protocol)** es un protocolo de **gestión de redes** utilizado para supervisar y administrar dispositivos de red como routers, switches, servidores, impresoras y otros dispositivos compatibles. SNMP permite que un sistema de gestión de red recoja información de estos dispositivos, los configure y supervisione su estado.

---

## 👉 ¿Qué hace SNMP?

- **Monitorea dispositivos de red**: Permite obtener datos sobre el estado y el rendimiento de los dispositivos, como el uso de CPU, la cantidad de tráfico en un puerto, o el estado de la memoria.
- **Configura dispositivos**: Se pueden cambiar configuraciones de los dispositivos de red de manera remota (por ejemplo, habilitar o deshabilitar puertos o interfaces).
- **Notifica eventos**: Los dispositivos pueden enviar trap messages al sistema de gestión para notificar eventos importantes, como un fallo de hardware o un alto consumo de recursos.

---

## 🛠️ Componentes clave de SNMP:

1. **Agente SNMP**: Es el software que corre en los dispositivos de red (routers, switches, servidores, etc.). Recibe las solicitudes del sistema de gestión y proporciona la información solicitada.
2. **Administrador SNMP (SNMP Manager)**: Es el sistema o software que monitorea y controla los dispositivos. Recibe datos y puede enviar solicitudes de modificación a los agentes SNMP.
3. **MIB (Management Information Base)**: Es una base de datos estructurada que contiene los objetos gestionables de un dispositivo. Los objetos se identifican mediante **OID (Object Identifier)**. MIB define qué información puede ser consultada o modificada.
4. **Traps**: Son mensajes enviados desde el dispositivo hacia el administrador SNMP cuando ocurren eventos o condiciones específicas (por ejemplo, un error o un cambio de estado).

---

## 🎯 Funcionamiento básico de SNMP:

1. El **administrador SNMP** envía una solicitud a un agente **SNMP** para obtener información sobre el estado del dispositivo o cambiar alguna configuración.
2. El **agente SNMP** responde con la información solicitada, que puede incluir datos de rendimiento, configuraciones o estadísticas.
3. Si ocurre un evento importante, el **agente SNMP** puede enviar un **trap** al administrador SNMP para notificar un cambio o un problema, como un fallo de dispositivo.

---

## 📝 Versiones de SNMP:

- **SNMPv1**: La primera versión, con seguridad limitada. Usa **comunidades** (pares de lectura/escritura) para autenticar los dispositivos.
- **SNMPv2c**: Mejora en velocidad y funcionalidades, pero también con seguridad limitada. También usa comunidades.
- **SNMPv3**: La versión más segura, que incluye **autenticación** y **cifrado** para proteger los datos que se intercambian entre el administrador y los agentes.

---

## 🚩 Ventajas y desventajas de SNMP:

✅ **Ventajas**:

- **Estándar abierto**: SNMP es un protocolo ampliamente soportado por casi todos los dispositivos de red.
- **Escalabilidad**: Permite gestionar redes grandes y complejas.
- **Flexibilidad**: Puede obtener y modificar configuraciones de una gran variedad de dispositivos.

❌ **Desventajas**:

- **Seguridad**: Las versiones anteriores (SNMPv1 y SNMPv2) no tienen buenas características de seguridad, aunque SNMPv3 mejora esto.
- **Complejidad de configuración**: Puede ser complejo configurar correctamente y gestionar SNMP en redes grandes, especialmente al configurar traps y MIBs personalizados.

---

:::tip Dato Adicional
SNMP es ampliamente utilizado en herramientas de gestión de red como **Nagios**, **Zabbix** o **PRTG Network Monitor** para supervisar el estado de la infraestructura de red y hacer diagnósticos.
:::
