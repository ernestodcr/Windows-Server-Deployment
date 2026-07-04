# 🖥️ Windows Server Deployment

Este repositorio contiene la documentación técnica y el despliegue del servidor principal de la empresa TecnoSoluciones S.A. utilizando el sistema operativo Windows Server 2022.

## 📥 1. Despliegue e Instalación del Sistema Operativo
Se realizó el aprovisionamiento base del servidor de la oficina configurando el entorno bajo los requisitos de hardware recomendados:

* **Creación de la Máquina:** Se configuró un entorno virtual con 4 GB de memoria RAM, 2 procesadores virtuales (vCPUs) y un disco duro dinámico de 50 GB.
* **Instalación Visual:** Se utilizó la imagen ISO oficial para realizar una instalación limpia seleccionando el modo **Experiencia de escritorio**, garantizando la disponibilidad de ventanas e interfaz gráfica para la gestión de la empresa.
* **Credenciales de Seguridad:** Se estableció la cuenta del usuario maestro `Administrador` bajo políticas de contraseña seguras (`Tecno2026`).

---

## 📡 2. Identidad Corporativa y Red Estática (SRV-WIN-01)
Se configuraron los datos básicos de la máquina para adaptarla a la red fija de la empresa:

* **Nombre de Equipo:** Se quitó el nombre raro que venía de fábrica y se le puso el nombre oficial corporativo `SRV-WIN-01`.
* **IP Fija de la Oficina:** Se bloqueó la IP automática y se configuró a mano la dirección estática `10.0.2.16` para que los empleados la encuentren siempre en el mismo sitio.
* **DNS Local:** Se configuró el número de bucle interno `127.0.0.1` en el servidor DNS preferente, preparando al sistema para coordinar los nombres de la oficina en las siguientes fases.


