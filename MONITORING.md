Protocolo de Monitorización y Control
Este framework está diseñado para pasar de la documentación a la vigilancia activa. Para asegurar que los riesgos identificados en la Matriz de Activos están bajo control, el equipo técnico debe implementar los siguientes tres niveles de monitorización:

1. Control de Ejecución (Enforcement)

• Acción: Integrar el archivo `policies/retention_policy.json` en los servicios de limpieza (Cron Jobs/Cloud Functions).

• Monitorización: El sistema debe emitir un log cada vez que se ejecute una purga de datos. Si un activo marcado como "Crítico" supera su TTL sin ser borrado, el sistema debe disparar una alerta de alta prioridad.

2. Monitorización de Acceso (Observabilidad)

• Acción: Mapear las etiquetas de clasificación de la `matriz_activos_datos.csv` con los logs de acceso de la base de datos (Audit Logs).

• Monitorización: Crear un tablero (Dashboard) que identifique patrones de acceso inusuales sobre activos clasificados como Sensibles o Críticos. Cualquier desviación del RBAC definido debe ser notificada al Oficial de Cumplimiento.

3. Verificación de Integridad (Auditoría Inmutable)

• Acción: Utilizar el Commit History de este repositorio como el registro oficial de cambios en la estrategia de seguridad.

• Monitorización: Revisión trimestral de que las reglas vigentes en el código coinciden con la última versión aprobada en este repositorio. Cualquier cambio no autorizado en los archivos de este framework se considera un hallazgo de auditoría.

---

Este protocolo asegura que el cumplimiento no sea una foto estática, sino un proceso dinámico y auditable.
