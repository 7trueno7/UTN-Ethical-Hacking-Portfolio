# Final 1: Diseño de Topología de Red Segura

### Descripción del Proyecto
Este proyecto consistió en el diseño de una topología de red híbrida desde cero, con un enfoque primordial en la resiliencia, la escalabilidad y la seguridad. El objetivo fue crear una infraestructura que no solo permitiera la conectividad, sino que también implementara múltiples capas de defensa para proteger la red de amenazas.

### Componentes y Metodología
La topología se diseñó en Cisco Packet Tracer y cuenta con los siguientes elementos principales:
- **Routers:** Dos routers Cisco 2911 para redundancia de conexión a internet.
- **Firewall:** Un firewall dedicado como primera línea de defensa para el control y filtrado del tráfico.
- **Switches de Capa 3:** Un switch principal (Cisco 3560) para enrutamiento interno y cinco switches secundarios para el acceso de los hosts.
- **Hosts:** Cinco grupos de 16 PCs, segmentados lógicamente para optimizar la seguridad y el rendimiento.

### Estrategias de Seguridad Implementadas
Se integraron varias medidas de seguridad en el diseño para crear una defensa en profundidad:
- **Redundancia:** Dos routers conectados a distintos ISPs para asegurar la continuidad del servicio.
- **Firewall:** Implementación de un dispositivo de seguridad que realiza filtrado de tráfico, NAT y puede actuar como un IPS.
- **Control de Acceso Centralizado:** Uso de un servidor de autenticación para gestionar el acceso a los dispositivos de red.
- **Segmentación de Red:** Creación de VLANs lógicas para aislar el tráfico y minimizar el impacto de un posible incidente de seguridad.
- **Listas de Control de Acceso (ACLs):** Configuración de reglas para filtrar el tráfico entre las VLANs y evitar accesos no autorizados.
- **Seguridad en Puertos:** Habilitación de la seguridad de puertos para vincular direcciones MAC a puertos específicos, previniendo la conexión de dispositivos no autorizados.
- **Seguridad en Hosts:** Políticas de protección en las PCs, incluyendo antivirus, firewalls locales y gestión de parches.

### Conclusiones y Habilidades Demostradas
Este proyecto demostró mi capacidad para diseñar, planificar e implementar una topología de red compleja desde una perspectiva de seguridad. Las habilidades clave demostradas incluyen el conocimiento de la arquitectura de red, el diseño de defensa en profundidad, la segmentación de red y la configuración de controles de seguridad de la capa 2 y 3.
