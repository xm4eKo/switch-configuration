---
title: SSH
sidebar_position: 5
---

# SSH (Secure Shell)

✅ **SSH (Secure Shell)** es un **protocolo de red de capa de aplicación** que permite **conectarse de forma segura a otro dispositivo a través de una red insegura** (como Internet). Está definido en **RFC 4251**.

Su función principal es **proveer acceso remoto cifrado a la línea de comandos (shell)** de un servidor o equipo.

---

## 👉 ¿Para qué sirve SSH?

- Acceder y administrar servidores de forma remota (muy usado en sistemas Linux/Unix).
- Transferir archivos de manera segura (por ejemplo, usando **SCP** o **SFTP**, que funcionan sobre SSH).
- Redireccionar puertos o hacer **túneles cifrados**.
- Autenticar usuarios y ejecutar comandos en máquinas remotas de forma segura.

---

## 🛠️ ¿Cómo funciona?

1. El cliente SSH inicia una conexión al servidor SSH (normalmente en el **puerto 22/TCP**).
2. Se establece un **canal cifrado** usando algoritmos de criptografía de clave pública.
3. El servidor verifica la identidad del cliente mediante:
   - Usuario y contraseña, o
   - Autenticación con **llaves públicas y privadas (par de claves)**, más segura y usada en entornos profesionales.
4. Una vez autenticado, el cliente accede al sistema remoto como si estuviera físicamente presente.

---

## 🎯 Características principales de SSH:

✅ **Cifrado de extremo a extremo**, protegiendo la confidencialidad e integridad de los datos.
✅ **Permite ejecución de comandos remotos**, no solo acceso a terminal interactiva.
✅ **Túneles SSH**: redirige tráfico de otras aplicaciones a través del canal cifrado.
✅ **Soporta compresión de datos** para conexiones más rápidas.

---

## 🚩 Ventajas sobre protocolos antiguos:

Antes de SSH se usaban protocolos como **Telnet**, **rlogin** o **FTP**, pero enviaban datos **sin cifrar** (en texto plano). SSH los reemplazó porque **cifra tanto las credenciales como la información transmitida**, evitando ataques como **interceptación o suplantación**.

---

## 📦 Comandos típicos (en Linux/macOS/WSL):

- Conexión:

```bash
ssh usuario@ip_servidor
```

- Copiar archivo (SCP):

```bash
scp archivo.txt usuario@ip_servidor:/ruta/destino
```

- Crear túnel:

```bash
ssh -L puerto_local:host_destino:puerto_destino usuario@ip_servidor
```

---

:::tip Dato Adicional
SSH es extensible y tiene variantes como OpenSSH (implementación libre y muy popular) o PuTTY (cliente SSH muy usado en Windows).
:::
