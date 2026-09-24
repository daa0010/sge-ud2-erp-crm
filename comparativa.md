# Comparativa Técnica de Sistemas ERP y CRM

---

## 1. Datos

* **Propietario:** daa0010
* **Empresa asignada:** FitZone
* **Palabra del día:** Compañeros

---

## 2. Licencias y Modelos

### Diferencias entre Software Libre (FSF), Código Abierto (OSI) y Propietario

* **Software Libre (Free Software Foundation - FSF):** 
Está centrado en defender la libertad y los derechos de los usuarios y de la comunidad. Garantiza el control total sobre el programa a través de cuatro libertades fundamentales: usar, estudiar, distribuir y modificar el software. Sus principales características son:
  * **Código fuente accesible y auditable**
  * **Soberanía e independencia del usuario**
  * **Libre redistribución y modificación sin restricciones**

* **Código Abierto (Open Source Initiative - OSI):** Es el modelo de desarrollo basado en la colaboración abierta. El código fuente es consultable, modificable y distribuible por cualquier persona. Aunque el código sea gratuito, el software puede implicar costes adicionales. Sus principales características son:
  * **Código fuente accesible**
  * **Modificable y distribuible**
  * **Colaboración comunitaria**
  * **Generalmente más económico**

* **Software Propietario:** Requiere pago por licencia de uso. Suele ser más profesional en interfaz, rendimiento y servicios. Cuenta con soporte técnico especializado de la empresa desarrolladora. Sus principales características son:
  * **Código fuente privado**
  * **Licencias de pago**
  * **Soporte técnico profesional**
  * **Mayor inversión inicial**
---

### Por qué «libre» no equivale a «gratuito»

El software libre garantiza la **libertad** de uso, modificación y distribución, no que sea gratuito. 

En el ámbito empresarial de los sistemas ERP/CRM, la adquisición de una licencia con coste cero no implica coste cero de propiedad, ya que tiene los siguientes costes:
* **Costes de implantación y parametrización:** Adaptación de las reglas de negocio, flujos y catálogo del sistema a la operativa de la empresa.
* **Infraestructura y despliegue:** Costes derivados de servidores, alojamiento en la nube, copias de seguridad, redes y seguridad perimetral.
* **Soporte y mantenimiento:** Necesidad de contratar especialistas externos, consultoras o destinar personal técnico interno para parches, migraciones y resolución de incidencias.
* **Formación del personal:** Capacitación del equipo de administración, recepción y monitores para operar la plataforma eficientemente.

---

### Implicaciones prácticas: Edición Community frente a Enterprise

* **Edición Community:** Software libre/abierto (sin coste de licencia directa). Incluye la funcionalidad básica del núcleo, carece de soporte técnico oficial con SLA, y las migraciones entre versiones mayores deben realizarse manualmente o mediante herramientas de la comunidad.
* **Edición Enterprise:** Software propietario bajo suscripción comercial. Añade módulos avanzados (contabilidad localizada completa, apps móviles oficiales, automatizaciones complejas), soporte directo del fabricante con tiempos de respuesta garantizados y herramientas automatizadas para migración de datos.

### Licencias de los cuatro productos analizados y sus consecuencias

| Producto | Tipo de Sistema | Modelo | Licencia Exacta | Consecuencias Prácticas |
| :--- | :--- | :--- | :--- | :--- |
| **Odoo Community** | ERP Libre | Open-Core | **GNU LGPLv3** | Permite crear módulos privados sin liberar su código fuente; la empresa asume la gestión interna o externa de parches y migraciones al no contar con soporte oficial del fabricante. |
| **Microsoft Dynamics 365** | ERP Propietario | SaaS Comercial | **Propietaria (EULA / Microsoft Customer Agreement)** | Código inaccesible, coste periódico por usuario/mes, soporte técnico directo con SLA, pero alta dependencia del ecosistema Microsoft (*vendor lock-in*). |
| **SuiteCRM** | CRM Libre | Open Source | **GNU AGPLv3** | Si la empresa modifica el núcleo del CRM y ofrece acceso a través de la red a usuarios externos o terceros, debe poner el código modificado a su disposición bajo los mismos términos AGPL. |
| **Salesforce Sales Cloud** | CRM Propietario | SaaS Comercial | **Propietaria (Main Services Agreement - MSA)** | Despliegue 100% dependiente de la nube del proveedor; no permite modificar el código base ni auditar el almacenamiento físico de datos, sujeto a cuotas mensuales recurrentes. |