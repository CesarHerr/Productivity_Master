# DEC-69 — Alcance de correcciones históricas

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por respuesta del PO: las tres opciones consultadas. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. DEC-69 parcialmente resuelta.

El PO necesita poder corregir tiempo registrado, resultado de un compromiso y justificación en una jornada histórica cerrada. Se mantiene corrección justificada y auditada sin reapertura, conservación de historial, actualización de estadísticas actuales y preservación de revisiones originales. La justificación de la corrección es distinta del texto histórico que se corrige y cumple validación aprobada DEC-65.

Confirmar estos tres ámbitos no aprueba todas las transiciones de resultados, introducir PENDIENTE en una jornada CERRADA, alterar fechas o reasignar compromisos, ni convertir corrección en reapertura autorizada para el mismo día. Tampoco se presume corrección automática del estado de tarea general. Esas consecuencias deben decidirse explícitamente.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC69-01 | El procedimiento de corrección de una jornada histórica CERRADA contempla corregir tiempo registrado sin reabrirla, con justificación y auditoría. Límites del nuevo valor y efectos cuantitativos concretos quedan pendientes. | DEC-69, alcance aprobado; RF-028; RN-20; CA-JOR-16/25. |
| CA-DEC69-02 | El procedimiento contempla corregir el resultado de un compromiso histórico, con justificación y auditoría sin reapertura; la aprobación de este ámbito no habilita todas las transiciones ni dejar compromisos PENDIENTES por inferencia. | DEC-69; RN-20; CA-DEC62-41. |
| CA-DEC69-03 | El procedimiento contempla corregir una justificación histórica, distinguiéndola de la justificación obligatoria de la acción de corrección. No sustituye silenciosamente el valor previo. | DEC-69; RN-20; CA-DEC65-09. |
| CA-DEC69-04 | Cada corrección aplicada conserva trazabilidad de valor anterior y nuevo con la justificación de la acción, mantiene CERRADA y actualiza estadísticas actuales conservando revisiones originales e historial. No fija mecanismo técnico. | DEC-69; RN-20/RN-28; RNF-002; CA-JOR-16/17; CA-DEC65-09. |

CA-DEC69-01 a CA-DEC69-04 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Pendientes: transiciones permitidas de resultados, efectos en tarea/progreso y destino de reprogramación, validación del tiempo corregido, formato de auditoría, tratamiento de fallos/concurrencia y cambios de categorías históricas. No se definen fórmulas ni implementación. PRD draft.

## Corrección de COMPLETADO erróneo — CONFIRMADA

El PO aprueba corregir un compromiso histórico marcado COMPLETADO por error a CANCELADO o REPROGRAMADO, con categoría y explicación. Se mantiene justificación de la acción de corrección, auditoría, valores anteriores/nuevos y jornada CERRADA sin reapertura. La categoría/explicación corresponde a la resolución corregida; no se prescribe usar campos compartidos para ambas justificaciones.

REPROGRAMADO conserva requisito de fecha destino RN-06; no se decide aún creación, reutilización, modificación o anulación del compromiso de destino. La aprobación de la transición no autoriza aplicar un cambio que ignore esas consecuencias pendientes ni cambios automáticos en estado de tarea. Otras transiciones históricas siguen pendientes.

## CA-DEC69-05 a CA-DEC69-07 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC69-05 | Un compromiso histórico COMPLETADO por error puede corregirse a CANCELADO mediante corrección justificada/auditada, con categoría y explicación para la resolución, sin reabrir la jornada. | DEC-69, aprobación explícita PO; RN-05/RN-20; CA-DEC69-02/04. |
| CA-DEC69-06 | Puede corregirse de COMPLETADO erróneo a REPROGRAMADO con categoría, explicación y fecha destino, por el procedimiento auditado sin reapertura; el tratamiento del compromiso de destino permanece pendiente y no se infiere. | DEC-69; RN-05/RN-06/RN-20; RF-026/RF-027. |
| CA-DEC69-07 | La corrección conserva el resultado previo y el nuevo, con justificación/auditoría, actualiza estadísticas actuales según reglas aprobadas y conserva revisiones originales e historial. | DEC-69; RN-28; CA-DEC69-04; CA-JOR-17. |

CA-DEC69-05 a CA-DEC69-07 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. No se aprueban otras transiciones, manejo del destino, fórmulas nuevas o cambios automáticos en tarea. PRD draft.

## Destino de corrección a REPROGRAMADO — CONFIRMADO

El PO aprueba crear una continuación vinculada a la misma tarea si no existe una correspondiente en destino. Si existe un compromiso potencialmente coincidente, mostrarlo y pedir decisión explícita, sin duplicarlo ni modificarlo silenciosamente. La forma exacta de identificar y resolver coincidencias sigue PENDIENTE y se relaciona con DEC-67. No se presupone reutilizar, fusionar, reemplazar o anular el candidato.

La aprobación no determina asignación a fechas futuras, destinos históricos cerrados, recurrencias o cálculo de restantes; se conservan las condiciones previas y el alcance del ejemplo cuantitativo. Tampoco decide consistencia conjunta entre la corrección original y creación/vinculación destino ante fallo o abandono: no se generaliza automáticamente CA-DEC62-17.

## CA-DEC69-08 a CA-DEC69-10 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC69-08 | Al corregir un compromiso a REPROGRAMADO, si no existe una continuación correspondiente en destino, se crea una vinculada a la misma tarea y al origen de la reprogramación. Fecha destino sigue obligatoria; identificación de correspondencia pendiente. | DEC-69, aprobación PO; RN-06/RN-11; CA-DEC62-01/09; DEC-67 pendiente. |
| CA-DEC69-09 | Si existe un compromiso potencialmente coincidente, se presenta al usuario y se solicita decisión explícita antes de modificarlo o crear un duplicado. No se selecciona automáticamente una forma de resolver la coincidencia. | DEC-69; RN-26 como antecedente; DEC-67 pendiente. |
| CA-DEC69-10 | La gestión del destino no duplica avances previos ni altera silenciosamente el compromiso coincidente; conserva identidad de tarea y trazabilidad de origen/destino. | DEC-69; RN-11/RN-26; CA-DEC62-06/09. |

CA-DEC69-08 a CA-DEC69-10 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Coincidencias exactas, decisiones disponibles, transacción funcional completa ante fallo/abandono y estados de destino quedan pendientes; no implementación. PRD draft.

## Aplicación conjunta origen/destino — CONFIRMADA

El PO aprueba que la corrección histórica del origen a REPROGRAMADO y la creación o vinculación del destino se confirmen conjuntamente. Mientras falte resolver una coincidencia, no se aplica la corrección. Abandonar o fallar no deja cambios parciales de esa operación. No se prescribe mecanismo técnico ni se aprueba por esta garantía una opción concreta para resolver coincidencias.

La vinculación debe corresponder a una decisión explícita cuando se detecte coincidencia; el alcance exacto de esa decisión sigue pendiente DEC-67. La garantía conserva valores previos y nuevos, auditoría, revisiones originales y momentos reales según reglas existentes; no revierte operaciones independientes realizadas fuera de este procedimiento.

## CA-DEC69-11 a CA-DEC69-14 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC69-11 | La confirmación válida aplica conjuntamente la corrección del origen a REPROGRAMADO y la creación o vinculación correspondiente del destino; no se confirma solo una parte. | DEC-69, aprobación PO; CA-DEC69-06/08/09. |
| CA-DEC69-12 | Si hay una coincidencia pendiente de decisión explícita, la corrección del origen y sus cambios de destino no se aplican. No se decide por defecto reutilizar, fusionar o reemplazar el candidato. | DEC-69; CA-DEC69-09; DEC-67 pendiente. |
| CA-DEC69-13 | Abandonar este procedimiento sin confirmar no aplica los cambios preparados al origen o destino, ni crea una continuación parcial. | DEC-69, garantía aprobada PO. |
| CA-DEC69-14 | Si falla la aplicación conjunta, no quedan parcialmente aplicadas la corrección del origen o la creación/vinculación de destino de esa operación. No se prescribe mecanismo técnico. | DEC-69, garantía aprobada PO; RN-12/RNF-003 como antecedentes propuestos, sin promoverlos en bloque. |

CA-DEC69-11 a CA-DEC69-14 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Identificación/alternativas de coincidencias, efectos en tarea y manejo de comunicación/reintentos/concurrencia quedan pendientes. PRD draft, sin implementación.
