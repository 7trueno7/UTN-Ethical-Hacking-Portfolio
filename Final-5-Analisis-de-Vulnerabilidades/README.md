# Final 5: Análisis de Vulnerabilidades en Metasploitable 2

### Descripción del Proyecto
Este proyecto práctico tuvo como objetivo identificar y analizar fallos de seguridad en un entorno de laboratorio controlado. Se utilizó la máquina virtual **Metasploitable 2** como objetivo de un escaneo de vulnerabilidades para descubrir debilidades críticas, altas y medias.

### Metodología
Se estableció un entorno de laboratorio seguro utilizando **VirtualBox** con dos máquinas virtuales:
1.  **Kali Linux** (máquina atacante).
2.  **Metasploitable 2** (máquina objetivo).

La red se configuró manualmente para garantizar la comunicación con **IPs estáticas** (10.0.0.10 para Kali y 10.0.0.20 para Metasploitable 2). Una vez verificada la conectividad con un `ping`, se procedió a realizar un escaneo completo de servicios y puertos utilizando la herramienta **Nmap** (`nmap -sV -p- 10.0.0.20`).

### Hallazgos y Análisis de Vulnerabilidades

El escaneo reveló múltiples servicios en ejecución, varios de los cuales presentan vulnerabilidades conocidas que podrían ser explotadas.

#### 1. Servicio FTP (vsftpd 2.3.4)
* **Nivel de Vulnerabilidad:** Crítico.
* **Análisis:** Esta versión del servidor FTP tiene un *backdoor* oculto que permite a un atacante obtener acceso de `root` y controlar completamente el sistema.
* **Recomendación:** Actualizar el servicio a una versión más reciente o deshabilitarlo si no es necesario.

#### 2. Servicio de Samba (smbd 3.X)
* **Nivel de Vulnerabilidad:** Crítico.
* **Análisis:** Esta versión de Samba es vulnerable a un fallo que permite la ejecución de comandos a distancia sin necesidad de autenticación, lo que podría llevar a una toma de control total del sistema.
* **Recomendación:** Actualizar a una versión de Samba más segura o cerrar los puertos si el servicio no se utiliza.

#### 3. Servicio UnrealIRCd
* **Nivel de Vulnerabilidad:** Crítico.
* **Análisis:** Esta versión contiene un *backdoor* que permite a los atacantes ejecutar comandos de forma remota en el servidor, lo que puede ser utilizado para ganar acceso `root` y comprometer el sistema.
* **Recomendación:** Actualizar el servidor o deshabilitar el servicio para evitar accesos no autorizados.

#### 4. Servicio Telnet
* **Nivel de Vulnerabilidad:** Alto.
* **Análisis:** El protocolo Telnet envía credenciales de usuario y contraseña en texto plano. Un atacante podría interceptar fácilmente este tráfico para robar las credenciales.
* **Recomendación:** Deshabilitar Telnet y utilizar un protocolo seguro como **SSH** para todas las conexiones remotas.

### Conclusión
Este ejercicio práctico demostró mi capacidad para configurar un entorno de laboratorio, usar herramientas de escaneo de vulnerabilidades y analizar los hallazgos para recomendar soluciones de seguridad. Este proceso es fundamental para la **identificación de riesgos** en cualquier infraestructura de red.
