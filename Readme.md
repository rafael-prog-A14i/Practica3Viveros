PRUEBAcat << 'EOF' > Readme.md
# Documentación Práctica 3 ADBD

### Descripción de las Entidades

*   **Vivero:** Representa las distintas instalaciones físicas o tiendas que tiene la empresa repartidas por diferentes lugares.
*   **Zona:** Son las distintas áreas o secciones en las que se divide un vivero concreto, como por ejemplo la zona exterior o el almacén.
*   **Producto:** Son las plantas, artículos de jardinería o de decoración que se venden y almacenan en las zonas de los viveros.
*   **Empleado:** Es el personal contratado por la empresa, que puede ser destinado a trabajar en diferentes zonas y viveros dependiendo de la temporada.
*   **Cliente:** Son los compradores de la empresa. Algunos de ellos forman parte del programa de fidelización especial *Tajinaste Plus* para recibir bonificaciones.
*   **Pedido:** Representa cada una de las compras o transacciones individuales que realiza un cliente y que es gestionada por un empleado concreto.

---

### Descripción y Dominio de los Atributos

**Entidad: Vivero**
*   **IDVivero:** Identificador único del vivero. *Dominio:* Código alfanumérico o número entero. (Ej: `VIV-01` o `104`).
*   **Latitud:** Coordenada geográfica para localizar el vivero. *Dominio:* Número decimal. (Ej: `28.4853`).
*   **Longitud:** Coordenada geográfica para localizar el vivero. *Dominio:* Número decimal. (Ej: `-16.3159`).

**Entidad: Zona**
*   **IDZona:** Identificador único de la zona dentro del sistema. *Dominio:* Código alfanumérico. (Ej: `ZON-EXT-01`).
*   **Latitud y Longitud:** Coordenadas específicas de la zona. *Dominio:* Números decimales.

**Entidad: Producto**
*   **IDProducto:** Código único que identifica al artículo. *Dominio:* Número entero o cadena de texto corta. (Ej: `PROD-9982`).

**Entidad: Empleado**
*   **IDEmpleado:** Número de identificación del trabajador (puede ser su DNI). *Dominio:* Cadena de texto de 9 caracteres. (Ej: `12345678A`).

**Entidad: Cliente**
*   **IDCliente:** Identificador único del comprador. *Dominio:* Cadena de texto (DNI) o número entero. (Ej: `CLI-005`).
*   **FechaAlta:** Día en el que el cliente se registró. *Dominio:* Fecha en formato DD/MM/AAAA. (Ej: `15/03/2025`).
*   **TajinastePlus:** Indica si pertenece al programa de fidelización. *Dominio:* Booleano (Verdadero/Falso). (Ej: `True`).
*   **NumCompras:** Volumen de compras o número de pedidos realizados. *Dominio:* Número entero positivo. (Ej: `12`).

**Entidad: Pedido**
*   **IDPedido:** Número de localizador de la compra. *Dominio:* Número entero secuencial. (Ej: `45902`).

**Atributos en las Relaciones**
*   **StockDisponible** *(en la relación Asignado)*: Cantidad de un producto que hay en una zona concreta. *Dominio:* Número entero mayor o igual a cero. (Ej: `150`).
*   **EpocaAnio** *(en la relación Histórico entre Empleado y Zona)*: Temporada en la que el empleado trabajó en esa zona. *Dominio:* Cadena de texto descriptiva. (Ej: `Primavera` o `Campaña Na
