Experto Universitario en Hacking Ético
Final número… 1
 Mi Primer Topología de Cero

Análisis de la topología

Dos routers conectados a los ISP diferentes: cada router necesita al menos un puerto WAN para conectarse a su respectivo ISP y un puerto LAN para conectarse al switch principal.
Switch de capa 3 principal: este switch debe tener puertos suficientes para conectar los dos routers y los cinco switches de capa 3 adicionales. Esto significa que necesita al menos 7 puertos (2 para los routers y 5 para los switches secundarios).
Cinco switches de capa 3 secundarios: cada uno debe conectar 16 PCs, lo que significa que deben tener al menos 16 puertos. Además, cada uno necesita un puerto adicional para conectarse al switch principal. En total cada switch requiere 17 puertos.

Topología Seleccionada y Diagrama

La topología de red diseñada es una topología híbrida, combina las ventajas de la topología en estrella extendida con la redundancia de una topología en malla parcial. Esta elección garantiza la resiliencia de la red, la escalabilidad y una gestión centralizada.

Descripción de los Componentes de la Topología

Routers (R1 y R2): Se han utilizado dos routers Cisco 2911. Cada uno está conectado a un proveedor de servicio (ISP) distinto, lo que proporciona redundancia de conexión a Internet. Si uno de los ISPs falla, el otro puede mantener la conectividad de la red.

Firewall: se ha implementado un firewall entre los routers y el switch principal. Este dispositivo es fundamental para controlar, filtrar e inspeccionar todo el tráfico que entra y sale de la red, actuando como la primera línea de defensa.

Switch de Capa 3 Principal: Este switch Cisco 3560 es el corazón de la red. Actúa como el punto central de agregación y se encarga del enrutamiento interno (inter-VLAN), facilitando la comunicación controlada entre los diferentes segmentos de la red.

Switches de Acceso (SW-1 a SW-5): Cinco switches Cisco 3560 están conectados al switch principal. Cada uno de estos switches está dedicado a un grupo de 16 PCs. Para cumplir con la consigna, cada switch es de 24 puertos o más, lo que permite conectar las 16 PCs y el enlace al switch principal.

Implementación de Seguridad: Dispositivos y Procesos

Firewall: No solo filtra tráfico, sino que también puede realizar NAT y actuar como un sistema de Prevención de Intrusiones (IPS), detectando y bloqueando automáticamente ataques conocidos.

Servidor de Autenticación: Se añade para centralizar el control de acceso a los dispositivos de red. Esto garantiza que solo los administradores autorizados puedan acceder a los routers y switches, y permite un registro detallado de las actividades de gestión.

Segmentación de la Red: Se crearán VLANs lógicas, una para cada grupo de 16 PCs. La segmentación aísla el tráfico y evita que un problema de seguridad en una sección se propague al resto de la red.

Listas de Control de Acceso: Se configurarán en el switch principal para filtrar el tráfico entre las VLANs, por ejemplo, una ACL puede impedir que las PCs accedan directamente a los recursos.

Seguridad en los Puertos: En los switches de acceso, esta función se habilitará para limitar el acceso a dispositivos no autorizados. La seguridad del puerto vinculará la dirección MAC de cada PC a su puerto, deshabilitando el puerto si se detecta un dispositivo desconocido.

Seguridad en los Hosts (PCs): La protección no termina en la red. Se implementarán políticas para asegurar que cada PC tenga:
Un antivirus/antimalware actualizado.
El firewall del sistema operativo activado.
El sistema operativo y las aplicaciones al día con los últimos parches de seguridad.
 
Conclusion
La topología diseñada cumple con todos los requisitos del ejercicio. Al combinar la redundancia de dos ISP y un firewall de borde con la segmentación de la red y medidas de seguridad en los hosts, se crea una infraestructura robusta, escalable y, sobre todo, segura. Este diseño es una representación práctica de cómo se aplica el concepto de defensa en profundidad en una red real.
