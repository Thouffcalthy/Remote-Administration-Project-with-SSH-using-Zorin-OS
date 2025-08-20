**Read this in other languages:**
- [Español](#proyecto-de-administración-remota-con-ssh)
- [English](#remote-administration-project-with-ssh)


# Proyecto de Administración Remota con SSH

## Introducción

**SSH (Secure Shell)** es un protocolo de red que permite la conexión segura y encriptada entre dos computadoras, generalmente para administrar remotamente un servidor o equipo. Fue diseñado para reemplazar protocolos inseguros como Telnet o FTP, que enviaban datos en texto plano. SSH permite:

- **Administración remota de servidores:** controlar servidores Linux, Windows o dispositivos en la nube desde cualquier lugar.  
- **Transferencia segura de archivos:** usando herramientas como `scp` o `sftp`.  
- **Túneles y port forwarding:** acceder de manera segura a servicios internos detrás de firewalls o NAT.  
- **Automatización y DevOps:** ejecutar comandos y scripts remotos.  
- **Seguridad:** cifrado fuerte y autenticación por clave pública para evitar accesos no autorizados.

---

## Recursos utilizados 🔑

- **Servidor:** Lenovo Ideapad S145 con Zorin OS 17, donde se instala y configura OpenSSH Server.  
- **Cliente:** Lenovo Ideapad 5 con Windows 11, desde donde se realizan las conexiones remotas usando PowerShell.  
- **Herramientas adicionales:**  
  - `scp` y `sftp` para transferencia de archivos.  
  - `rsync` y scripts Bash para automatización (etapas posteriores).  
  - Markdown para documentar cada paso del proyecto.

---

## Motivación del proyecto 🚀

Este proyecto surge del interés por **dominar la administración remota de sistemas**, un conocimiento fundamental para roles de DevOps, soporte técnico avanzado y administración de infraestructura TI. Practicar con SSH permite:

- Mejorar la seguridad en la administración de servidores.  
- Entender cómo funciona la comunicación cifrada entre cliente y servidor.  
- Automatizar tareas repetitivas y optimizar flujos de trabajo.

---

## Qué se espera aprender 🎯

Siguiendo un **plan de estudios de 12 semanas**, se pretende:

1. **Fundamentos:** instalación de SSH, conexión remota y comandos básicos.  
2. **Nivel intermedio:** automatización de tareas, sincronización de archivos y montaje de carpetas remotas.  
3. **Nivel avanzado:** túneles SSH, acceso seguro a servicios internos y despliegues de código.

Al finalizar el proyecto, se habrá desarrollado un **entorno práctico de administración remota**, documentado paso a paso, que demuestra habilidades concretas en la gestión segura de servidores Linux usando SSH.

---

## Sobre el proyecto 🧐

El proyecto consiste en **documentar, paso a paso, la instalación, configuración y prueba de un servidor SSH** en Zorin OS, incluyendo la conexión desde un cliente Windows, la ejecución de comandos básicos y la transferencia segura de archivos. Además, se integrará automatización y técnicas avanzadas en etapas posteriores, generando una **base sólida de conocimientos prácticos aplicables en el mundo profesional**.

## Documentación Semanal 📆

- [Semana 1: Instalación y prueba](Week1/Installation-and-testing.md) ✅
- [Semana 2: Configuración de SSH](Week2/SSH-Configuration.md) ✅
- Semana 3 (Pronto)


# Remote Administration Project with SSH

## Introduction

**SSH (Secure Shell)** is a network protocol that allows secure and encrypted connections between two computers, usually to remotely administer a server or workstation. It was designed to replace insecure protocols like Telnet or FTP, which transmitted data in plain text. SSH enables:

- **Remote server administration:** manage Linux, Windows, or cloud servers from anywhere.  
- **Secure file transfer:** using tools like `scp` or `sftp`.  
- **Tunnels and port forwarding:** securely access internal services behind firewalls or NAT.  
- **Automation and DevOps:** run remote commands and scripts.  
- **Security:** strong encryption and public key authentication to prevent unauthorized access.

---

## Resources used 🔑

- **Server:** Lenovo Ideapad S145 with Zorin OS 17, where OpenSSH Server is installed and configured.  
- **Client:** Lenovo Ideapad 5 with Windows 11, used to establish remote connections via PowerShell.  
- **Additional tools:**  
  - `scp` and `sftp` for file transfers.  
  - `rsync` and Bash scripts for automation (later stages).  
  - Markdown to document each step of the project.

---

## Project motivation 🚀

This project arises from the interest in **mastering remote system administration**, a key skill for DevOps roles, advanced technical support, and IT infrastructure management. Practicing with SSH allows:

- Enhancing server administration security.  
- Understanding how encrypted communication works between client and server.  
- Automating repetitive tasks and optimizing workflows.

---

## Expected learning outcomes 🎯

Following a **12-week curriculum**, the goals are:

1. **Fundamentals:** SSH installation, remote connection, and basic commands.  
2. **Intermediate level:** task automation, file synchronization, and remote folder mounting.  
3. **Advanced level:** SSH tunnels, secure access to internal services, and code deployment.

At the end of the project, a **practical remote administration environment** will be developed, documented step by step, demonstrating concrete skills in secure Linux server management using SSH.

---

## About the project 🧐

The project consists of **documenting, step by step, the installation, configuration, and testing of an SSH server** on Zorin OS, including connecting from a Windows client, executing basic commands, and securely transferring files. In later stages, automation and advanced techniques will be integrated, building a **solid foundation of practical knowledge applicable in professional environments**.

---

## Weekly Documentation 📆

- [Week 1: Installation and Testing](Week1/Installation-and-testing.md) ✅
- [Week 2: SSH Configuration](Week2/SSH-Configuration.md) ✅
- [Week 3](Coming soon)
