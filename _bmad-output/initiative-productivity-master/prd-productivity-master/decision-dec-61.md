# DEC-61 — Reapertura justificada del mismo día

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por declaración explícita del PO. **Criterios CA-DEC61-01 a CA-DEC61-04:** CONFIRMADOS. **CA-DEC61-05 a CA-DEC61-08:** CONFIRMADOS por aprobación explícita del PO. DEC-61 permanece parcialmente abierta.

El PO indica que, si cierra la jornada y luego quiere ingresar otra actividad ese día, debe poder reabrirla registrando justificación de la acción. Se confirma transición manual CERRADA → ABIERTA en este caso del mismo día, sin introducir estados adicionales.

## Cambio explícito respecto del descubrimiento

RN-20/DEC-20 y las fuentes anteriores describían corrección auditada sin reapertura. La nueva decisión permite una acción explícita de reapertura justificada para agregar actividad del mismo día. Sustituye la interpretación de una prohibición absoluta de reapertura; no aprueba reapertura de jornadas de fechas anteriores ni modificación de resultados históricos.

CA-JOR-16 y CA-JOR-25 continúan describiendo correcciones auditadas, que no reabren por sí mismas. CA-JOR-18 conserva el itinerario ordinario SIN_ABRIR → ABIERTA → CERRADA, ahora con la excepción explícita de DEC-61. Sus textos anteriores se conservan y esta diferencia se hace visible; no se cambian silenciosamente.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC61-01 | Para ingresar una actividad adicional del mismo día, el usuario puede solicitar explícitamente la reapertura de su jornada CERRADA; si se confirma válidamente, pasa a ABIERTA conservando su fecha. | DEC-61, nueva confirmación PO; estados CA-JOR-01. |
| CA-DEC61-02 | Sin justificación registrada no se permite confirmar la reapertura. No se exige categoría por inferencia; formato y validación exactos pendientes. | DEC-61, justificación exigida por PO. |
| CA-DEC61-03 | Ingresar una actividad no reabre silenciosamente: la reapertura es una acción explícita del usuario. | DEC-61; RN-01 como antecedente de control manual. |
| CA-DEC61-04 | Tras reabrir, la actividad se incorpora bajo las reglas aprobadas para ABIERTA; volver a cerrar requiere resolver compromisos y nueva confirmación manual. | FR-3; RN-03 a RN-06; CA-JOR-05/06/07/08; coordinación propuesta para DEC-61. |

## Pendientes

Si cerrar antes de terminar el día se permite sin restricciones adicionales; definición exacta de mismo día respecto de medianoche/zona horaria DEC-68; formato de justificación; presentación del historial de cierres sucesivos y reaperturas (su conservación ya fue confirmada); efecto en resúmenes/estadísticas; efecto estadístico del retiro de descanso al reabrir; número de reaperturas; tratamiento de cambios anteriores y eventual corrección auditada DEC-69. No habilitar jornadas de fechas anteriores por inferencia.

CA-DEC61-01 a CA-DEC61-04 fueron aprobados e incorporados al borrador; no se prescribe implementación. PRD draft.

## Historial de jornadas — CONFIRMADO por el PO

Se conserva cada apertura, cierre y reapertura con su momento real. Cada reapertura conserva su justificación. Los cierres anteriores no se reemplazan al reabrir o volver a cerrar. Se mantiene la distinción entre fecha de jornada y momentos reales de las acciones, sin prescribir formato, almacenamiento, precisión temporal ni interfaz.

**Origen:** aprobación explícita del PO durante DEC-61; antecedente CA-JOR-24 y RNF-002. No se aprueban reaperturas de fechas anteriores ni otros límites temporales. La decisión posterior sobre descanso se registra al final.

## CA-DEC61-05 a CA-DEC61-08 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC61-05 | Cada apertura, cierre y reapertura efectivamente realizados conserva un registro distinguible de la acción y su momento real. No se fija formato ni precisión temporal. | DEC-61, confirmación PO; CA-JOR-24. |
| CA-DEC61-06 | Cada reapertura conserva la justificación correspondiente vinculada a esa acción, sin sustituir la de una reapertura anterior. | DEC-61; CA-DEC61-02; RNF-002 como antecedente. |
| CA-DEC61-07 | Reabrir o volver a cerrar no reemplaza ni elimina los registros de cierres anteriores de la misma jornada. | DEC-61, nueva confirmación; RNF-002 como antecedente. |
| CA-DEC61-08 | Tras apertura, cierre, reapertura y nuevo cierre, el historial permite distinguir las cuatro acciones con sus momentos reales y la justificación de la reapertura, conservando la fecha de jornada. | DEC-61; CA-DEC61-01/04; CA-JOR-24. |

Los criterios CA-DEC61-05 a CA-DEC61-08 fueron aprobados e incorporados como CONFIRMADOS al borrador del PRD. La conservación de acciones no define cómo calcular estadísticas ni qué cierres cuentan para indicadores. Esas reglas siguen pendientes.

## Reapertura de descanso — precisión CONFIRMADA por el PO

Ante la pregunta sobre reabrir un día cerrado como descanso para agregar actividad, el PO elige retirar explícitamente la marca de descanso. En el caso de reapertura del mismo día previamente aprobado, se retira la marca; se mantienen reapertura explícita y justificación. No se aprueba reapertura de fechas anteriores ni una fórmula de penalización o recálculo estadístico.

El historial ya confirmado conserva el cierre anterior; retirar la marca vigente no elimina ese registro. La forma exacta de registrar el retiro, el efecto en estadísticas permanece pendiente. La coordinación se confirmó posteriormente: retiro y reapertura conjuntos, sin aplicación parcial ante fallo.

### CA-DEC61-09 a CA-DEC61-11 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC61-09 | En el caso aprobado del mismo día, reabrir una jornada cerrada como descanso para agregar actividad requiere retirar explícitamente la marca de descanso. | DEC-61, respuesta explícita PO; RN-23/CA-JOR-10 como antecedentes. |
| CA-DEC61-10 | La reapertura desde descanso conserva los requisitos de acción explícita y justificación; retirar la marca no abre por sí mismo una jornada silenciosamente. | DEC-61; CA-DEC61-01/02/03. |
| CA-DEC61-11 | Retirar la marca vigente de descanso no elimina el registro del cierre anterior ni los momentos y justificaciones ya conservados. No establece recálculo estadístico. | DEC-61; CA-DEC61-05 a CA-DEC61-08. |

Estos tres criterios fueron aprobados explícitamente por el PO e incorporados como CONFIRMADOS al borrador. El PRD sigue draft.

## Retiro de descanso y reapertura conjuntos — CONFIRMADO

El PO aprueba que retirar explícitamente la marca de descanso y reabrir la jornada se confirmen conjuntamente. Si falla la operación, la jornada permanece CERRADA y conserva su marca de descanso. No se prescribe mecanismo técnico. Se mantienen la acción explícita y la justificación ya aprobadas; no se altera el historial de cierres anteriores.

### CA-DEC61-12 a CA-DEC61-14 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC61-12 | Una confirmación válida del caso aprobado aplica conjuntamente la retirada explícita de la marca de descanso y la reapertura: el resultado es ABIERTA sin la marca vigente de descanso. | DEC-61, nueva aprobación PO; CA-DEC61-01/09/10. |
| CA-DEC61-13 | Si falla esa operación, la jornada permanece CERRADA y conserva la marca de descanso; no queda aplicada solo una de las dos acciones. | DEC-61, garantía aprobada por PO. |
| CA-DEC61-14 | La operación conjunta conserva la justificación de reapertura y los registros de cierres anteriores, sin eliminar el historial del descanso declarado. | DEC-61; CA-DEC61-05/06/07/11. |

CA-DEC61-12 a CA-DEC61-14 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Efectos estadísticos, detalles temporales y representación del historial siguen pendientes. PRD draft.
