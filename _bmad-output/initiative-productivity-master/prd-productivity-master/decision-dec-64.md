# DEC-64 — Días pasados vacíos nunca abiertos

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por aprobación explícita del PO. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. DEC-64 parcialmente resuelta.

Una fecha pasada que nunca se abrió y no tuvo compromisos asumidos no exige regularización ni se considera incumplimiento automáticamente. La condición no se aplica a un día que sí asumió compromisos aunque luego se resolvieran, cancelaran, reprogramaran o retiraran: su historial no se borra ni se confunde con nunca haber tenido compromisos. Esos días conservan regularización y cierre ya aprobados.

Esta decisión no cierra automáticamente una jornada SIN_ABRIR, no abre retroactivamente ni marca descanso por inferencia. No determina el tratamiento de una jornada vacía que sí se abrió y no cerró ni fórmulas/denominadores de consistencia.

## Criterios — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC64-01 | Una fecha pasada nunca abierta y sin compromisos asumidos no se identifica como obligatoria de regularización. | DEC-64, aprobación PO; contraste RN-08/CA-JOR-13. |
| CA-DEC64-02 | Ese día no se clasifica automáticamente como incumplimiento por ausencia de apertura o cierre. No fija fórmulas ni denominadores. | DEC-64, aprobación PO; DEC-63 pendiente. |
| CA-DEC64-03 | Resolver, cancelar, reprogramar o retirar compromisos no convierte una fecha que los tuvo en un día sin compromisos asumidos a efectos de esta excepción. | DEC-64; RN-19/RN-25; CA-JOR-13; RF-035. |
| CA-DEC64-04 | Aplicar esta excepción no abre/cierra la jornada automáticamente ni declara descanso; no agrega un estado efectivo adicional. | DEC-64; RN-01/RN-03; CA-JOR-01/03/07. |

CA-DEC64-01 a CA-DEC64-04 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Fechas vacías abiertas sin cerrar y jornadas esperadas para indicadores siguen pendientes. No implementación; PRD draft.

## Jornada abierta vacía sin cierre — CONFIRMADO

El PO aprueba que una jornada ABIERTA sin compromisos y sin cierre confirmado requiera cierre manual individual, incluso cuando su fecha haya pasado. No se considera incumplimiento de tareas por ausencia de compromisos. La consecuencia en indicadores de consistencia de cierres sigue pendiente DEC-63.

Esto precisa la excepción de días nunca abiertos: solo esos días vacíos están dispensados de regularización; una jornada abierta vacía conserva obligación de cierre. No se modifica RN-27 para definir por inferencia que esta jornada vacía bloquee revisión periódica: el alcance de jornada comprometida sigue pendiente.

### CA-DEC64-05 a CA-DEC64-07 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC64-05 | Una jornada ABIERTA sin compromisos no se cierra automáticamente ni queda dispensada de cierre manual. | DEC-64, aprobación PO; CA-JOR-07/09/21. |
| CA-DEC64-06 | Si su fecha ya pasó y sigue ABIERTA, requiere cierre manual individual conservando su fecha original y distinguiendo el momento real de cierre. | DEC-64; RN-08 como antecedente de fecha original; CA-JOR-24. |
| CA-DEC64-07 | Cerrar esa jornada vacía no cuenta como incumplimiento de tareas; no define su efecto en consistencia de cierres. | DEC-64; CA-JOR-09/21; DEC-63 pendiente. |

CA-DEC64-05 a CA-DEC64-07 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Fórmulas y bloqueo de revisiones por jornadas vacías abiertas siguen pendientes. PRD draft.

## Precisión posterior DEC-27 — CONFIRMADA

El PO aprueba ampliar el bloqueo de cierre periódico a toda jornada ABIERTA del período, incluso vacía. Sustituye la incertidumbre de bloqueo de abiertas vacías que se registró antes; fórmulas de consistencia siguen pendientes. Véase [DEC-27](decision-dec-27.md).
