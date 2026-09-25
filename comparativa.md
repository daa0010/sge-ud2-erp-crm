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

#### Fuentes consultadas
* Free Software Foundation (FSF): https://www.gnu.org/philosophy/free-sw.html 
* Open Source Initiative (OSI): https://opensource.org/osd 
* Odoo Licensing details: https://www.odoo.com/documentation/18.0/legal/licenses.html 
* SuiteCRM Project License (AGPLv3): https://suitecrm.com/about/license/ 

### Elección de Licencia para FitZone y Justificación

Para la cadena de gimnasios FitZone, la licencia más adecuada es **GNU LGPLv3**, adoptada a través de la solución **Odoo Community** (desplegada en un servidor VPS centralizado en la nube).

**Justificación técnica y económica para la empresa:**

1. **Eliminación del coste por puesto en plantilla:** FitZone cuenta con 40 trabajadores (monitores y personal de recepción). Optar por licencias propietarias por usuario/mes (como Microsoft Dynamics o Salesforce) supondría un coste operativo recurrente inasumible para una pyme provincial de 4 centros. La licencia LGPLv3 no cobra por usuario concurrente ni registrado, reduciendo el Coste Total de Propiedad (TCO) y permitiendo dar acceso a toda la plantilla.
2. **Ventaja del copyleft débil (LGPLv3):** A diferencia de licencias con copyleft fuerte, la LGPLv3 permite a FitZone desarrollar o integrar módulos específicos (por ejemplo, pasarelas de conexión con los tornos físicos de acceso de cada centro o lectores RFID) manteniéndolos de forma privada para su operativa interna, sin estar obligada legalmente a liberar su código fuente a la comunidad.
3. **Flexibilidad frente a la cláusula de red de la AGPL:** Al utilizar LGPLv3 para el núcleo de la gestión, la empresa evita los requerimientos de la AGPL relativos a la entrega de código frente al acceso de usuarios remotos a través de la red, facilitando el despliegue de portales web para socios y empleados con total tranquilidad jurídica.
4. **Independencia del proveedor (*Vendor Lock-in*):** Al tratarse de software de código abierto con una amplia comunidad y ecosistema de consultores, FitZone no queda cautiva de las políticas comerciales de un único fabricante propietario, manteniendo el control total sobre su base de datos relacional y su infraestructura.

## 3. Fichas Técnicas de los Productos Evaluados

### 3.1. ERP Libre: Odoo Community

* **Licencia exacta:** GNU Lesser General Public License versión 3 (GNU LGPLv3).
  * *Fuente:* [Odoo Licensing Documentation](https://www.odoo.com/documentation/18.0/legal/licenses.html)(Consulta: septiembre 2026). 
* **Versión vigente:** Odoo 18.0 (LTS).
  * *Fuente:* [Odoo Release Notes & GitHub Repository](https://github.com/odoo/odoo/releases)(Consulta: septiembre 2026).
* **Lenguaje del servidor:** Python (versión 3.10 o superior) y JavaScript / OWL (OpenWood Library) para la capa de presentación web.
  * *Fuente:* [Odoo Developer Documentation](https://www.odoo.com/documentation/18.0/developer/reference/backend.html)(Consulta: septiembre 2026). 
* **SGBD compatibles:** PostgreSQL exclusivamente (versiones 13.0 a 16.x recomendadas). No soporta MySQL, MariaDB ni Oracle de forma nativa.
  * *Fuente:* [Odoo Technical Specifications](https://www.odoo.com/documentation/18.0/administration/install.html)(Consulta: septiembre 2026). 
* **Modalidad de despliegue:** Instalación On-Premise (local) o alojamiento en infraestructura IaaS/VPS Cloud propia (Docker, Kubernetes o servidor dedicado).
  * *Fuente:* [Odoo On-Premise Installation Guide](https://www.odoo.com/documentation/18.0/administration/install/install.html)(Consulta: septiembre 2026).
* **Módulos principales:** Facturación básica, Inventario y Almacén, Punto de Venta (POS), Compras, Ventas, CRM integrado y Empleados (Recursos Humanos).
  * *Fuente:* [Odoo Apps Core Directory](https://apps.odoo.com/apps/modules)(Consulta: septiembre 2026).
* **Requisitos mínimos recomendados:** 
  * *Hardware:* 2 vCPU, 4 GB de memoria RAM (para 40 usuarios concurrentes ligeros) y almacenamiento de 40 GB SSD.
  * *Software:* Servidor Linux (Ubuntu Server 22.04 LTS / 24.04 LTS o Debian 12), servidor web proxy inverso (Nginx) y certificado SSL/TLS.
  * *Fuente:* [Odoo Deployment Architecture Guide](https://www.odoo.com/documentation/18.0/administration/install/deploy.html)(Consulta: septiembre 2026).

---

### 3.2. ERP Propietario: Microsoft Dynamics 365 Business Central

* **Licencia exacta:** Propietaria comercial por suscripción por usuario/mes (*Microsoft Customer Agreement* / Licenciamiento Cloud Solution Provider).
  * *Fuente:* [Microsoft Dynamics 365 Licensing Guide](https://www.microsoft.com/licensing/terms/productoffering/Dynamics365/MCA)(Consulta: septiembre 2026).
* **Versión vigente:** Dynamics 365 Business Central 2026 Release Wave (v24/v25).
  * *Fuente:* [Microsoft Learn - Dynamics 365 Release Plans](https://learn.microsoft.com/en-us/dynamics365/release-plans/)(Consulta: septiembre 2026).
* **Lenguaje del servidor:** C# (.NET Runtime) en el núcleo del servicio de aplicación y lenguaje propio AL (*Application Language*) para el desarrollo de extensiones y reglas de negocio.
  * *Fuente:* [Microsoft Learn - Developing in AL for Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview)(Consulta: septiembre 2026). 
* **SGBD compatibles:** Microsoft Azure SQL Database (en despliegue SaaS) o Microsoft SQL Server 2019 / 2022 Standard o Enterprise (en despliegue local On-Premise).
  * *Fuente:* [Microsoft Learn - System Requirements for Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/deployment/system-requirement-business-central-v24)(Consulta: septiembre 2026). 
* **Modalidad de despliegue:** Nube pública SaaS multi-inquilino (hospedado y gestionado íntegramente en Microsoft Azure) o implementación local On-Premise / Híbrida.
  * *Fuente:* [Microsoft Dynamics 365 Overview](https://dynamics.microsoft.com/es-es/business-central/overview/)(Consulta: septiembre 2026). 
* **Módulos principales:** Gestión financiera y contabilidad, Gestión de proyectos, Cadena de suministro y almacén, Ventas y servicio, Operaciones y Fabricación básica.
  * *Fuente:* [Business Central Capabilities Directory](https://learn.microsoft.com/en-us/dynamics365/business-central/across-business-functionality)(Consulta: septiembre 2026).
* **Requisitos mínimos recomendados:**
  * *Modalidad SaaS:* Acceso mediante navegador web compatible con HTML5 (Microsoft Edge, Google Chrome) y conexión a Internet estable (mínimo 1 Mbps por usuario concurrente).
  * *Modalidad On-Premise:* Servidor Windows Server 2022+, mínimo 4 núcleos de CPU, 16 GB de RAM dedicados a la instancia del servidor y almacenamiento SSD en RAID.
  * *Fuente:* [Microsoft Learn - Server Component Requirements](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/deployment/system-requirements)(Consulta: septiembre 2026).

---

### 3.3. CRM Libre: SuiteCRM

* **Licencia exacta:** GNU Affero General Public License versión 3 (GNU AGPLv3).
  * *Fuente:* [SuiteCRM License - SalesAgility](https://suitecrm.com/about/license/)(Consulta: septiembre 2026).
* **Versión vigente:** SuiteCRM 8.7.
  * *Fuente:* [SuiteCRM GitHub Releases Repository](https://github.com/salesagility/SuiteCRM-Core/releases)(Consulta: septiembre 2026). 
* **Lenguaje del servidor:** PHP (versión 8.2 o 8.3) sobre el framework Symfony en el backend y Angular / TypeScript en el frontend.
  * *Fuente:* [SuiteCRM 8 Technical Architecture](https://docs.suitecrm.com/8.x/developer/)(Consulta: septiembre 2026). 
* **SGBD compatibles:** MariaDB (10.4 a 10.11+) y MySQL (8.0+). No soporta nativamente PostgreSQL sin extensiones comunitarias no mantenidas.
  * *Fuente:* [SuiteCRM Compatibility Matrix](https://docs.suitecrm.com/8.x/admin/compatibility-matrix/)(Consulta: septiembre 2026). 
* **Modalidad de despliegue:** Instalación On-Premise o alojamiento en servidores web y contenedores Cloud propios (IaaS/VPS).
  * *Fuente:* [SuiteCRM Installation Guide](https://docs.suitecrm.com/8.x/admin/installation-guide/)(Consulta: septiembre 2026). 
* **Módulos principales:** Gestión de cuentas y contactos, Embudo de ventas (Oportunidades), Gestión de clientes potenciales (*Leads*), Automatización de campañas de marketing por correo, Módulo de casos y atención al cliente, Informes y diseñador de flujos de trabajo (*Workflow Engine*).
  * *Fuente:* [SuiteCRM User Documentation](https://docs.suitecrm.com/user/)(Consulta: septiembre 2026). 
* **Requisitos mínimos recomendados:**
  * *Hardware:* 2 vCPU, 4 GB de memoria RAM y 20 GB de espacio libre en disco SSD.
  * *Software:* Servidor Linux (Ubuntu Server o Rocky Linux), servidor HTTP Apache 2.4 o Nginx, PHP 8.2/8.3 con extensiones habilitadas (curl, zip, gd, mbstring, imap) y motor MariaDB 10.6+.
  * *Fuente:* [SuiteCRM System Requirements](https://docs.suitecrm.com/8.x/admin/installation-guide/downloading-installing/)(Consulta: septiembre 2026). 

---

### 3.4. CRM Propietario: Salesforce Sales Cloud

* **Licencia exacta:** Propietaria comercial bajo suscripción periódica por usuario (*Master Subscription Agreement* - MSA).
  * *Fuente:* [Salesforce Master Subscription Agreement Legal Terms](https://www.salesforce.com/company/legal/agreements/)(Consulta: septiembre 2026).
* **Versión vigente:** Salesforce 2026 Release Cycle (Spring '26 / Summer '26). Actualizaciones automáticas y continuas gestionadas por el fabricante tres veces al año.
  * *Fuente:* [Salesforce Trust & Maintenance Calendar](https://status.salesforce.com/)(Consulta: septiembre 2026).
* **Lenguaje del servidor:** Lenguaje propietario Apex (sintaxis orientada a objetos similar a Java) ejecutado en la plataforma multi-inquilino de Salesforce, y Lightning Web Components (LWC / JavaScript y HTML5) en el cliente.
  * *Fuente:* [Salesforce Developer Documentation - Apex Reference](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/)(Consulta: septiembre 2026).
* **SGBD compatibles:** Base de datos relacional propietaria y gestionada internamente por la plataforma en la nube (arquitectura subyacente basada en clústeres de Oracle Database y tecnologías NoSQL optimizadas). No permite conexión directa por JDBC/ODBC a la base de datos física; el acceso a datos se efectúa exclusivamente mediante lenguajes propietarios de consulta como SOQL (*Salesforce Object Query Language*) y APIs REST/SOAP.
  * *Fuente:* [Salesforce Multi-tenant Architecture Whitepaper](https://developer.salesforce.com/docs/atlas.en-us.fundamentals.meta/fundamentals/bi_arch_1.htm)(Consulta: septiembre 2026). 
* **Modalidad de despliegue:** Exclusivamente Nube SaaS (*Software as a Service*) multi-inquilino. No existe opción de instalación local On-Premise ni de despliegue en servidores privados.
  * *Fuente:* [Salesforce Sales Cloud Overview](https://www.salesforce.com/es/products/sales-cloud/overview/)(Consulta: septiembre 2026). 
* **Módulos principales:** Gestión de clientes potenciales (*Lead Management*), Fichas unificadas de contactos y cuentas (*Account & Contact Management*), Oportunidades y cotizaciones de venta, Automatización de procesos comerciales (*Salesforce Flow*), Analítica e informes en tiempo real, e integración de IA predictiva/generativa (*Agentforce*).
  * *Fuente:* [Salesforce Sales Cloud Features](https://www.salesforce.com/products/sales-cloud/features/)(Consulta: septiembre 2026).
* **Requisitos mínimos recomendados:**
  * *Hardware/Servidor:* Sin requisitos de servidor local (infraestructura 100% remota).
  * *Cliente:* Equipo cliente o dispositivo móvil con navegador web moderno con soporte TLS 1.3 (Google Chrome, Mozilla Firefox, Microsoft Edge o Apple Safari) y conexión a Internet de banda ancha.
  * *Fuente:* [Salesforce Technical Requirements Documentation](https://help.salesforce.com/s/articleView?id=sf.getstart_browsers_sfx.htm&type=5)(Consulta: septiembre 2026).

---

## 4. Fe de Erratas del Tema 2

En este apartado se contrastan afirmaciones recogidas en la presentación del Tema 2 frente a la documentación técnica oficial y la realidad actual.

---

### Errata 1: Compatibilidad de SGBD en SuiteCRM

* En la diapositiva *«Soluciones CRM: Libres y Propietarias»*, se afirma sobre SuiteCRM: *«Compatible con MySQL, MariaDB y SQL Server»*.
* Pero en la versión vigente (SuiteCRM 8.x), el soporte para **Microsoft SQL Server está completamente descatalogado**. SuiteCRM 8 solo es compatible con motores relacionales **MariaDB** (versiones 10.4 a 10.11+) y **MySQL** (versión 8.0).
* **Fuente oficial:** [SuiteCRM Documentation - Compatibility Matrix 8.x](https://docs.suitecrm.com/8.x/admin/compatibility-matrix/)

---

### Errata 2: Confusión entre Software Libre y Código Abierto

* En la diapositiva titulada *«Software Libre vs Propietario»*, se define directamente en la primera columna el concepto de *«Código Abierto»*, tratándolos como términos equivalentes y sinónimos.
* El **Software Libre (FSF)** y el **Código Abierto (OSI)** parten de principios distintos. El Software Libre es un movimiento de base filosófica y ética que exige el cumplimiento incondicional de las 4 libertades del usuario. El Código Abierto (*Open Source*) es un enfoque metodológico y comercial centrado en las ventajas técnicas del desarrollo colaborativo y la calidad del software, sin priorizar el componente ético.
* **Fuente oficial:** [Free Software Foundation (FSF) - Por qué el «código abierto» pierde el punto de vista del software libre](https://www.gnu.org/philosophy/open-source-misses-the-point.es.html)

---

## 5. Matriz de Decisión y Recomendación para FitZone

### 5.1. Totales Ponderados de las Opciones Evaluadas

Los criterios, pesos y puntuaciones detalladas se encuentran registrados en el archivo `matriz_decision.csv`. El cálculo del total ponderado (escala de 1 a 5) para cada alternativa candidata es:

* **Odoo Community (ERP + CRM): 4,40 / 5**
  * Cálculo: $(5 \cdot 0,25) + (5 \cdot 0,20) + (4 \cdot 0,15) + (4 \cdot 0,15) + (3 \cdot 0,15) + (5 \cdot 0,10) = 1,25 + 1,00 + 0,60 + 0,60 + 0,45 + 0,50 = 4,40$
* **Microsoft Dynamics 365 (SaaS): 3,55 / 5**
  * Cálculo: $(2 \cdot 0,25) + (5 \cdot 0,20) + (4 \cdot 0,15) + (5 \cdot 0,15) + (4 \cdot 0,15) + (1 \cdot 0,10) = 0,50 + 1,00 + 0,60 + 0,75 + 0,60 + 0,10 = 3,55$
* **SuiteCRM (+ ERP externo): 2,85 / 5**
  * Cálculo: $(4 \cdot 0,25) + (2 \cdot 0,20) + (3 \cdot 0,15) + (1 \cdot 0,15) + (3 \cdot 0,15) + (4 \cdot 0,10) = 1,00 + 0,40 + 0,45 + 0,15 + 0,45 + 0,40 = 2,85$

---

### 5.2. Justificación de las Puntuaciones por Criterio

#### Criterio 1: Coste Total de Propiedad (TCO) para 40 empleados (Peso: 25%)
* **Odoo Community (5/5):** Licencia LGPLv3 sin coste recurrente por usuario. Para los 40 trabajadores de FitZone, la inversión se reduce al coste de un servidor VPS y la parametrización inicial, maximizando el retorno de inversión.
* **MS Dynamics 365 (2/5):** Su modelo de licenciamiento comercial por usuario nominal al mes eleva exponencialmente el coste operativo anual para una plantilla de 40 personas, resultando económicamente inviable para una pyme provincial.
* **SuiteCRM (4/5):** No cobra licencias por usuario, pero al carecer de módulos de gestión empresarial global, FitZone se vería obligada a costear licencias o integraciones con un software contable independiente.

#### Criterio 2: Integración nativa ERP + CRM (sin silos de datos) (Peso: 20%)
* **Odoo Community (5/5):** Comparte un único motor relacional (PostgreSQL) y una capa de datos común. La ficha del socio en el CRM se conecta en tiempo real con el Punto de Venta (TPV) de recepción, la facturación y la contabilidad.
* **MS Dynamics 365 (5/5):** Plataforma madura que integra de forma integral las áreas de finanzas, ventas y operaciones en un ecosistema unificado.
* **SuiteCRM (2/5):** Es exclusivamente un CRM. Resolver la fragmentación de FitZone exigiría desarrollar y mantener conectores API para sincronizar los cobros y socios con un ERP externo, perpetuando el riesgo de silos.

#### Criterio 3: Gestión multisede y reservas de socios (B2C) (Peso: 15%)
* **Odoo Community (4/5):** Dispone de arquitectura multi-sucursal nativa y módulos de portal web y TPV para validar membresías y gestionar reservas de clases en los cuatro locales desde una misma base de datos.
* **MS Dynamics 365 (4/5):** Muy potente para redes comerciales multisede, aunque adaptar su interfaz para reservas ágiles en mostrador deportivo requiere desarrollos a medida.
* **SuiteCRM (3/5):** Permite registrar el historial de socios, pero carece de un TPV de mostrador y de un sistema nativo de gestión de aforos de clases grupales.

#### Criterio 4: Gestión interna de RRHH y turnos (B2E) (Peso: 15%)
* **Odoo Community (4/5):** Incluye de serie módulos de Empleados, Asistencias (fichajes) y Planificación de turnos, esenciales para organizar a los monitores y recepcionistas entre los centros.
* **MS Dynamics 365 (5/5):** Ofrece herramientas corporativas completas para la gestión avanzada de talento, nóminas y control horario.
* **SuiteCRM (1/5):** No dispone de módulo de Recursos Humanos, cuadrantes de trabajo ni gestión de turnos para empleados.

#### Criterio 5: Facilidad de despliegue y mantenimiento técnico (Peso: 15%)
* **Odoo Community (3/5):** Al ser una implantación local/VPS administrada, FitZone debe asumir la configuración de copias de seguridad, actualizaciones del sistema operativo y securización del servidor.
* **MS Dynamics 365 (4/5):** Modelo SaaS donde Microsoft gestiona infraestructura, parches y disponibilidad, aunque la complejidad de parametrización funcional es alta.
* **SuiteCRM (3/5):** Requiere despliegue sobre servidor LAMP/LEMP y mantenimiento periódico de la base de datos y dependencias de PHP.

#### Criterio 6: Independencia del proveedor y control de datos (Peso: 10%)
* **Odoo Community (5/5):** Código accesible bajo LGPLv3 y base de datos PostgreSQL estándar. FitZone puede cambiar de proveedor de soporte técnico en cualquier momento sin perder sus datos ni su software.
* **MS Dynamics 365 (1/5):** Dependencia total (*vendor lock-in*) de la nube y políticas comerciales de Microsoft. Los datos residen en bases de datos propietarias de difícil extracción directa.
* **SuiteCRM (4/5):** Código libre AGPLv3 con base de datos MariaDB/MySQL estándar y accesible.

---

### 5.3. Recomendación Final y Análisis de Riesgos

La solución recomendada para **FitZone** es **Odoo Community** desplegado en un servidor VPS centralizado en la nube, al obtener la puntuación ponderada más alta (**4,40 frente a 3,55 y 2,85**). 

Esta elección unifica la gestión de las cuatro sedes en una base de datos centralizada sin incurrir en costes por licencia para los 40 trabajadores, resolviendo de raíz el problema de los silos de datos y habilitando el acceso multisede para los socios.

#### Evaluación de Riesgos Asociados

1. **Coste Total de Propiedad (TCO) y costes ocultos:** Aunque no existen pagos por licencia, FitZone debe asumir los costes de parametrización inicial, el coste mensual del servidor VPS y la contratación de un consultor o soporte técnico especializado para el despliegue de módulos comunitarios.
2. **Dependencia del proveedor (*Vendor Lock-in*):** El riesgo es mínimo frente a soluciones propietarias gracias a la licencia LGPLv3 y el uso de PostgreSQL. No obstante, existe dependencia técnica de la comunidad Odoo (OCA) o de la consultora externa contratada para las adaptaciones complejas.
3. **Soporte técnico y SLA:** La edición Community no cuenta con acuerdos de nivel de servicio (SLA) oficiales del fabricante. Cualquier caída del sistema en recepción debe mitigarse contratando una empresa de mantenimiento externa con tiempos de respuesta contractualmente pactados.
4. **Migración futura y evolución:** Las actualizaciones entre versiones mayores de Odoo no son automáticas en la edición Community. FitZone debe prever el uso de herramientas comunitarias como OpenUpgrade o planificar ventanas de mantenimiento para migrar la base de datos sin comprometer la operativa de los gimnasios.