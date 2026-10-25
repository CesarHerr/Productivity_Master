# DEC-60 — Operaciones antes de apertura

**Decisión:** CONFIRMADA por el PO al aceptar la opción presentada: planificar antes de abrir; exigir ABIERTA para registrar avances o confirmar cumplimiento. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. Fecha: 2026-10-11.

En SIN_ABRIR se permite planificar. Registrar avances y confirmar cumplimiento requiere apertura manual previa. No se confirma apertura implícita por esas acciones. No se resuelven asignaciones futuras, creación de compromisos antes de apertura, duplicados, recurrencias ni registro de trabajo sin compromiso. Tampoco se decide actividad después de cierre o corrección histórica.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC60-01 | En SIN_ABRIR se permite planificar sin que esa acción abra automáticamente la jornada. | DEC-60; RN-01; RF-011. |
| CA-DEC60-02 | En SIN_ABRIR no se permite registrar avances; la operación exige apertura manual previa. | DEC-60; RF-016; RN-01. |
| CA-DEC60-03 | En SIN_ABRIR no se permite confirmar cumplimiento de compromisos o tareas de esa jornada. | DEC-60; RN-15; RF-018/RF-025. |
| CA-DEC60-04 | Tras abrir manualmente, se permiten registro de avances y confirmación de cumplimiento bajo sus reglas ya aprobadas; abrir no confirma cumplimiento por sí mismo. | DEC-60; RN-01/RN-15; CA-JOR-03/04/05. |

Los cuatro criterios fueron aprobados e incorporados como CONFIRMADOS al borrador del PRD. No se modifica el registro histórico de discovery. PRD draft.
