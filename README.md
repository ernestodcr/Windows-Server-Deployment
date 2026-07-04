# 🖥️ Windows Server Deployment

Este repositorio contiene la documentación técnica y el despliegue del servidor principal de la empresa TecnoSoluciones S.A. utilizando el sistema operativo Windows Server 2022.

## 📥 1. Despliegue e Instalación del Sistema Operativo
Se realizó el aprovisionamiento base del servidor de la oficina configurando el entorno bajo los requisitos de hardware recomendados:

* **Creación de la Máquina:** Se configuró un entorno virtual con 4 GB de memoria RAM, 2 procesadores virtuales (vCPUs) y un disco duro dinámico de 50 GB.
* **Instalación Visual:** Se utilizó la imagen ISO oficial para realizar una instalación limpia seleccionando el modo **Experiencia de escritorio**, garantizando la disponibilidad de ventanas e interfaz gráfica para la gestión de la empresa.
* **Credenciales de Seguridad:** Se estableció la cuenta del usuario maestro `Administrador` bajo políticas de contraseña seguras (`Tecno2026`).

## 📡 2. Identidad Corporativa y Red Estática (SRV-WIN-01)
Se configuraron los datos básicos de la máquina para adaptarla a la red fija de la empresa:

* **Nombre de Equipo:** Se quitó el nombre raro que venía de fábrica y se le puso el nombre oficial corporativo `SRV-WIN-01`.
* **IP Fija de la Oficina:** Se bloqueó la IP automática y se configuró a mano la dirección estática `10.0.2.16` para que los empleados la encuentren siempre en el mismo sitio.
* **DNS Local:** Se configuró el número de bucle interno `127.0.0.1` en el servidor DNS preferente, preparando al sistema para coordinar los nombres de la oficina en las siguientes fases.

## 👑 3. Instalación del Rol de Active Directory (AD DS)
Se procedió a incorporar los componentes lógicos necesarios para dotar al servidor de la capacidad de centralizar la gestión de identidades y recursos de la red corporativa:

* **Adición del Rol Empresarial:** Se utilizó el asistente del Administrador del Servidor para integrar de forma limpia los *Servicios de dominio de Active Directory* (AD DS).
* **Preparación de Herramientas Operativas:** La instalación desplegó con éxito las consolas de administración remota, las herramientas de línea de comandos de AD y el motor de administración de directivas de grupo, dejando el nodo preparado para la posterior promoción del dominio.



