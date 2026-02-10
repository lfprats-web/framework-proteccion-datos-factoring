# 🛡️ Nexus-Fin: Framework de Arquitectura de Datos para Onboarding Crítico

**Proyecto:** Arquitectura de Seguridad y Gobernanza para Factoring (Ley 21.719).
**Estado:** 🟢 En Curso

## 🎯 Objetivos del Proyecto
* **Gobernanza por Diseño:** La seguridad y el cumplimiento normativo (Compliance) son el núcleo del flujo del dato, no periféricos.
* **Mitigación de Riesgos:** Blindaje de activos críticos (Credenciales Bancarias y Mandatos) mediante desacoplamiento y control de grano fino.
* **Eficiencia Operativa (FinOps):** Optimización del ciclo de vida del dato para reducir deuda técnica.

## 🌐 Contexto y Alcance
El sistema gestiona la ingesta desde una App de Onboarding hasta BigQuery, garantizando:
1.  **Soberanía del Dato:** Control absoluto sobre la residencia de la PII.
2.  **Audit Literacy:** Registros inmutables y linaje de datos para auditoría.
3.  **Resiliencia Legal:** Ejecución automatizada del Derecho al Olvido.

## 📂 Estructura del Repositorio (Compliance as a Code)
Este repositorio utiliza archivos CSV como "Single Source of Truth" para las políticas de gobierno:

* `matriz_activos.csv`: Catálogo de riesgos y clasificación de sensibilidad.
* `roadmap.csv`: Estado de implementación de controles técnicos.

---
*Arquitectura diseñada para cumplimiento de Normativa UAF y Ley de Protección de Datos.*