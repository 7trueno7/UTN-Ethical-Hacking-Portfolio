# Final 2: Análisis y Solución de Problemas en Topología de Red

### Descripción del Proyecto
Este final se centró en la identificación y resolución de problemas comunes en una topología de red. El objetivo fue analizar un diagrama de red (Figura 1) y proponer soluciones lógicas y físicas para mitigar fallos y mejorar la resiliencia y la seguridad de la infraestructura.

### Problemas Identificados y Soluciones Propuestas

**1. Conflicto de Direccionamiento IP**
* **Problema:** Las redes Alfa y Omega tenían el mismo rango de direccionamiento IP, lo que causaba un conflicto grave que impedía la comunicación a través del router.
* **Solución:** Se asignó un rango de direcciones IP diferente a la red Omega (ej. 192.168.2.0/24) y se configuraron correctamente las puertas de enlace en todos los hosts y el router.

**2. Configuración Incorrecta de la Puerta de Enlace**
* **Problema:** Los hosts no podían comunicarse con redes externas porque la puerta de enlace predeterminada no estaba configurada correctamente, resultando en la pérdida de paquetes.
* **Solución:** Se revisó y configuró la dirección IP de la interfaz del router en cada host para asegurar que el tráfico pudiera salir correctamente de cada red.

**3. Punto Único de Fallo y Redundancia**
* **Problema:** El router que interconectaba ambas redes representaba un punto único de fallo. Una avería en el dispositivo o en su conexión detendría toda la comunicación entre las redes.
* **Solución:** Se propuso la implementación de un segundo router en paralelo para crear un diseño de alta disponibilidad. Se utilizaría un protocolo de redundancia de primer salto (como HSRP o VRRP) para crear una puerta de enlace virtual y mitigar el riesgo de interrupción del servicio.

### Habilidades Clave Demostradas
* **Análisis Crítico:** Capacidad para identificar problemas de diseño en una topología de red.
* **Resolución de Problemas:** Propuesta de soluciones técnicas y lógicas para mitigar riesgos.
* **Conocimiento de Redes:** Sólida comprensión de conceptos como direccionamiento IP, enrutamiento, puertas de enlace y redundancia.
