# Framework de Protección de Datos (Factoring)

![Compliance](https://img.shields.io/badge/Compliance-Ley%2021.719-green)
![Security](https://img.shields.io/badge/Security-AES--256-blue)
![Data_Governance](https://img.shields.io/badge/Governance-BigQuery-orange)

Este repositorio es un Framework de Arquitectura de Privacidad, que centraliza y automatiza el Cumplimiento

---

## Objetivos del Proyecto
* **Gobernanza por Diseño:** Seguridad integrada desde la captura del dato.
* **Audit Literacy:** Trazabilidad total e inmutable para entes reguladores (UAF/SII).
* **Compliance as a Code:** Políticas de seguridad que viven en el repositorio.
* Este framework permite configurar disparadores (triggers) que validen que cualquier cambio en la estructura de datos no viole las reglas de cumplimiento definidas en este repositorio antes de pasar a producción.

## Activos y Roadmap
Los datos maestros de este framework se encuentran en formato abierto para auditoría técnica:
* 📂 [Ver Matriz de Riesgos](./Matriz%20de%20Activos%20de%20Datos%203025ff23dab9805b84b2e05f189f23b8.csv)
* 📂 [Ver Roadmap de Implementación](./Roadmap%20de%20Implementación%203025ff23dab980efaa7ccd31f921cffd.csv)

## Especificaciones de Seguridad
### 1. Enmascaramiento Dinámico
Implementación de **RBAC** (Control de Acceso Basado en Roles) para ocultar PII (RUT/Email) en entornos comerciales, manteniendo la visibilidad solo para Riesgo y Cumplimiento.

### 2. Ciclo de Vida del Dato
Políticas de purga automática (TTL) para documentos sensibles (Carpeta Tributaria) reduciendo la superficie de ataque tras el parsing.

### 3. Validación Legal: 
Revisar la [Matriz de Activos](./Matriz%20de%20Activos%20de%20Datos%203025ff23dab9805b84b2e05f189f23b8.csv), para confirmar que los niveles de sensibilidad y plazos de retención se alinean con su política interna.

### 4. Integración Técnica:
El equipo de TI debe consultar el archivo [retention_policy.json](./policies/retention_policy.json) para programar las tareas de purga automática en los servidores de producción.

### 5. Certificación de Auditoría: 
Este repositorio deja evidencia inmutable ante entes reguladores (UAF/SII) para demostrar la trazabilidad del diseño de privacidad.

### 6. Personalización:
Si el modelo de negocio escala, puede solicitar ajustes en la matriz para incluir nuevos activos de datos sin necesidad de reescribir la documentación base.


**Arquitecto Legal:** lfprats-web | **Tecnologías:** BigQuery, GitHub Actions, Python.
