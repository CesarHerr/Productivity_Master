# DEC-65 — Categorías iniciales de justificación

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por aprobación del PO. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. DEC-65 parcialmente resuelta.

Lista inicial aprobada para cancelar o reprogramar compromisos: Falta de tiempo; Cambio de prioridad; Dependencia o bloqueo; Salud o descanso; Imprevisto personal; Error de planificación; Otro. Se conserva explicación textual obligatoria para todas las categorías, incluida Otro, conforme RN-05/DEC-05.

No se amplía el requisito de categoría automáticamente a cancelación definitiva de tarea, reapertura, retiro o correcciones auditadas. Elegir Salud o descanso no declara un día de descanso ni sustituye su proceso aprobado.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC65-01 | Al cancelar o reprogramar un compromiso, se ofrece la lista inicial aprobada: Falta de tiempo, Cambio de prioridad, Dependencia o bloqueo, Salud o descanso, Imprevisto personal, Error de planificación y Otro. | DEC-65, aprobación explícita PO; RF-026; RN-05. |
| CA-DEC65-02 | No se confirma cancelación o reprogramación de un compromiso sin seleccionar categoría y aportar explicación textual, incluida categoría Otro. No se fija longitud ni validación detallada todavía. | DEC-65; DEC-05; RF-026; RN-05. |
| CA-DEC65-03 | Seleccionar Salud o descanso solo clasifica la justificación del compromiso; no declara descanso ni cierra la jornada automáticamente. | DEC-65; RN-23; CA-JOR-10/11/22. |

CA-DEC65-01 a CA-DEC65-03 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Validación textual exacta, cambios/personalización de categorías y requisitos específicos para otras acciones siguen pendientes. No implementación; PRD draft.

## Validación textual mínima — CONFIRMADA

El PO aprueba rechazar explicación vacía o compuesta únicamente por espacios para cancelar/reprogramar compromisos, sin exigir longitud mínima adicional. Una explicación no vacía que contenga al menos un carácter distinto de espacio satisface esta validación mínima; no se prescribe evaluación automática de calidad ni mecanismo técnico. Categoría y fecha destino cuando corresponda conservan sus condiciones.

### CA-DEC65-04 a CA-DEC65-06 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC65-04 | No se permite confirmar cancelación o reprogramación de compromiso con explicación vacía. | DEC-65, nueva aprobación PO; RN-05/RF-026; CA-DEC65-02. |
| CA-DEC65-05 | Una explicación compuesta solo por espacios se considera inválida, aun con categoría seleccionada. | DEC-65, nueva aprobación PO; RN-05. |
| CA-DEC65-06 | Una explicación con al menos un carácter distinto de espacio no se rechaza por longitud mínima adicional; categoría, destino y demás condiciones siguen aplicándose. | DEC-65; CA-DEC65-02; RN-06/RF-027. |

CA-DEC65-04 a CA-DEC65-06 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. No se extiende automáticamente esta validación a cancelación definitiva, reapertura o correcciones. Máximo de longitud, tratamiento de otros caracteres blancos y demás formatos no se fijan aquí. PRD draft.

## Validación en otras acciones — CONFIRMADA

El PO aprueba aplicar a cancelación definitiva de tarea, reapertura de jornada y correcciones auditadas la misma validación textual mínima: justificación no vacía ni formada solo por espacios, sin longitud mínima adicional y sin exigir categoría. Esto no elimina categoría/texto obligatorios para cancelaciones o reprogramaciones de compromisos preparadas dentro de una cancelación definitiva.

La validación no amplía la autorización para corregir campos históricos ni reabrir fechas distintas de las aprobadas. Retiro de compromiso sigue fuera de este bloque hasta definir su encaje.

### CA-DEC65-07 a CA-DEC65-10 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC65-07 | Confirmar cancelación definitiva de tarea exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; mantiene las demás condiciones aprobadas. | DEC-65, aprobación PO; CA-DEC62-22/28/31. |
| CA-DEC65-08 | Confirmar reapertura autorizada de jornada exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; no amplía el alcance de reapertura. | DEC-65; CA-DEC61-01/02. |
| CA-DEC65-09 | Una corrección auditada permitida exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; auditoría y alcance pendiente se conservan. | DEC-65; RN-20; CA-JOR-16/25; DEC-69 pendiente. |
| CA-DEC65-10 | La ausencia de categoría en la justificación de cancelación definitiva no dispensa categoría y explicación para cada compromiso que se prepare cancelar dentro del procedimiento. | DEC-65; RN-05; CA-DEC62-27/28; CA-DEC65-02. |

CA-DEC65-07 a CA-DEC65-10 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. No se fija longitud máxima, tecnología ni reglas de corrección todavía pendientes. PRD draft.
