# 🛡️ Nexus-Fin: Framework de Protección de Datos (Factoring)

![Compliance](https://img.shields.io/badge/Compliance-Ley%2021.719-green)
![Security](https://img.shields.io/badge/Security-AES--256-blue)
![Data_Governance](https://img.shields.io/badge/Governance-BigQuery-orange)

Este repositorio contiene la arquitectura de seguridad y gobernanza para el onboarding crítico de Factoring, diseñado para cumplir con la **Ley 21.719** y normativas de la **UAF**.

## 🎯 Objetivos del Proyecto
* **Gobernanza por Diseño:** Seguridad integrada en el núcleo del flujo del dato.
* **Audit Literacy:** Capacidad de respuesta inmediata ante auditorías mediante registros inmutables.
* **Compliance as a Code:** Políticas de retención y enmascaramiento ejecutables.

## 📊 Activos y Roadmap
Los datos maestros de este framework se encuentran en formato abierto para auditoría técnica:
* [Ver Matriz de Riesgos](./Matriz%20de%20Activos%20de%20Datos%203025ff23dab9805b84b2e05f189f23b8.csv): Clasificación de PII y controles de seguridad.
* [Ver Roadmap de Implementación](./Roadmap%20de%20Implementación%203025ff23dab980efaa7ccd31f921cffd.csv): Fases de despliegue técnico.

## 🛠️ Especificaciones Técnicas
### Enmascaramiento Dinámico (RBAC)
Se implementa un control de acceso basado en roles donde el dato sensible (RUT/Email) solo es visible de forma parcial para roles comerciales, manteniendo la integridad para procesos de Riesgo.

### Política de Retención
Los activos tienen un ciclo de vida automatizado (ej. PDFs de Carpetas Tributarias con TTL de 1 hora) para minimizar la superficie de ataque.

---
**Arquitecto Responsable:** lfprats-web  
*Documentación generada para fines de Compliance y Auditoría Técnica.*
