# DEC-27 — Bloqueo de cierre periódico por jornadas abiertas

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por aprobación explícita del PO. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO.

El PO aprueba ampliar RN-27/DEC-27: toda jornada ABIERTA cuya fecha pertenezca al período impide confirmar el cierre de su revisión semanal o mensual hasta que se cierre, aunque no tenga compromisos. Se refiere al cierre de la revisión; no se prescribe impedir consultar sus datos o preparar la reflexión.

## Diferencia explícita y reglas conservadas

RN-27 original bloqueaba por jornadas comprometidas pendientes de regularización. Se mantiene esa condición, incluidas fechas históricas con compromisos y sin cierre aunque estén SIN_ABRIR, según CA-JOR-13/15/20. La nueva aprobación agrega abiertas vacías. No sustituye el bloqueo anterior por un filtro solo ABIERTA.

Fechas pasadas nunca abiertas y sin compromisos siguen dispensadas de regularización por CA-DEC64-01 y no se convierten en bloqueo por esta ampliación. Las abiertas vacías requieren cierre manual según CA-DEC64-05/06. No se prescriben fórmulas ni se aprueba cierre automático del período al desaparecer bloqueos.

## Criterios — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC27-01 | Si existe una jornada ABIERTA con fecha dentro del período, no se permite confirmar cierre de su revisión semanal o mensual, aunque tenga cero compromisos o todos resueltos. | DEC-27, ampliación explícita RN-27; RF-031; CA-DEC64-05/06. |
| CA-DEC27-02 | La ampliación conserva el bloqueo por jornadas del período con compromisos asumidos y sin cierre, incluso SIN_ABRIR; no se restringe el filtro solo a ABIERTA. | RN-27/DEC-27; RF-031; CA-JOR-13/15/20. |
| CA-DEC27-03 | Cerrar las jornadas bloqueantes elimina ese motivo de bloqueo, pero no cierra automáticamente la revisión ni dispensa su confirmación manual y demás condiciones aprobadas. | DEC-27; RN-10; RF-029/RF-031; DEC-10. |

CA-DEC27-01 a CA-DEC27-03 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Efecto en consistencia/fórmulas sigue pendiente DEC-63; coordinación de compromisos entre períodos DEC-73 sigue pendiente. PRD draft, sin implementación.
