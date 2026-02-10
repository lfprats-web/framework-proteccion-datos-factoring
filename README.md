# Framework de Protección de Datos (Factoring)

![Compliance](https://img.shields.io/badge/Compliance-Ley%2021.719-green)
![Security](https://img.shields.io/badge/Security-AES--256-blue)
![Data_Governance](https://img.shields.io/badge/Governance-BigQuery-orange)

Este repositorio centraliza la arquitectura de seguridad y gobernanza para el onboarding crítico de Factoring, alineado con la **Ley 21.719**.

## Objetivos del Proyecto
* **Gobernanza por Diseño:** Seguridad integrada desde la captura del dato.
* **Audit Literacy:** Trazabilidad total e inmutable para entes reguladores (UAF/SII).
* **Compliance as a Code:** Políticas de seguridad que viven en el repositorio.

## Activos y Roadmap
Los datos maestros de este framework se encuentran en formato abierto para auditoría técnica:
* 📂 [Ver Matriz de Riesgos](./Matriz%20de%20Activos%20de%20Datos%203025ff23dab9805b84b2e05f189f23b8.csv)
* 📂 [Ver Roadmap de Implementación](./Roadmap%20de%20Implementación%203025ff23dab980efaa7ccd31f921cffd.csv)

## Especificaciones de Seguridad
### 1. Enmascaramiento Dinámico
Implementación de **RBAC** (Control de Acceso Basado en Roles) para ocultar PII (RUT/Email) en entornos comerciales, manteniendo la visibilidad solo para Riesgo y Cumplimiento.

### 2. Ciclo de Vida del Dato
Políticas de purga automática (TTL) para documentos sensibles (Carpeta Tributaria) reduciendo la superficie de ataque tras el parsing.

---
**Arquitecto:** lfprats-web | **Tecnologías:** BigQuery, GitHub Actions, Python.

---

## Instrucciones para Implementación y Automatización (TI)

Este repositorio no es solo documental; está estructurado para ser consumido por procesos de CI/CD y automatización de seguridad:

### 1. Consumo de Políticas vía API
Los desarrolladores pueden consumir las reglas de retención y enmascaramiento directamente desde la URL "Raw" de GitHub para alimentar scripts de limpieza automática:
* **Endpoint de Retención:** `https://github.com/lfprats-web/framework-proteccion-datos-factoring/raw/main/policies/retention_policy.json`

### 2. Sincronización de Gobernanza (SSOT)
Se recomienda mapear los campos definidos en `matriz_activos.csv` con las etiquetas de clasificación de datos en la nube (ej. Google Cloud Data Catalog o AWS Glue) para automatizar el cumplimiento de privacidad desde el origen.

### 3. Validaciones de Seguridad (GitHub Actions)
Este framework permite configurar disparadores (triggers) que validen que cualquier cambio en la estructura de datos no viole las reglas de cumplimiento definidas en este repositorio antes de pasar a producción.
