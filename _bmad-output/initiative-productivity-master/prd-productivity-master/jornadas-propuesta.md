# Ciclo de vida de jornadas — decisiones y criterios en revisión

**Fecha:** 2026-10-11. **Estado documental:** borrador. Las decisiones y CA-JOR-01 a CA-JOR-17 están CONFIRMADOS por el PO. Los criterios adicionales CA-JOR-18 a CA-JOR-25 están CONFIRMADOS por aprobación explícita posterior del PO. No se amplía DEC-62.

## Registro de precisiones con identificadores existentes

Esta nota complementa el registro histórico de discovery, sin modificarlo. Reutiliza los IDs oficiales existentes para el mismo tema; no crea ni renumera decisiones. Las precisiones de esta fase prevalecen sobre propuestas anteriores.

| Decisión existente | Precisión CONFIRMADA del PO | Trazabilidad |
|---|---|---|
| DEC-01, DEC-03 | Catálogo exhaustivo del ciclo ordinario: SIN_ABRIR, ABIERTA, CERRADA. Apertura y cierre manuales conservan sus reglas. | RF-011/RF-025; RN-01/RN-03. |
| DEC-23 | Descanso representado como jornada CERRADA identificada explícitamente como descanso. Resolver o trasladar justificadamente compromisos antes de confirmarlo; no penaliza por sí mismo cumplimiento. | RF-015; RN-23; RN-04 a RN-06. |
| DEC-08 | Fechas históricas con compromisos asumidos y sin cierre requieren regularización individual, incluso si nunca se abrieron, conservando fecha original. | RF-028; RN-08; RN-27/RF-031 como vínculo periódico. |
| DEC-64 | Jornada con cero compromisos puede cerrarse manualmente sin contar como incumplimiento. DEC-64 sigue parcialmente abierta para jornadas vacías no cerradas y jornadas esperadas. | RF-025; RN-03; DEC-63 fórmulas pendientes. |
| DEC-03 | Resolver todos los compromisos no cierra automáticamente: requiere confirmación manual. | RF-025; RN-03. |

**Diferencias respecto de la propuesta anterior:** PENDIENTE_APERTURA se sustituye por SIN_ABRIR; no es estado adicional. Descanso no deja una jornada abierta: su resultado es CERRADA con identificación de descanso. La propuesta de dispensar cierre a descansos sin abrir queda descartada; la precisión posterior del PO exige apertura manual antes de cierre, también para descanso. Se prohíbe expresamente SIN_ABRIR → CERRADA.

## CA-JOR-01 a CA-JOR-17 — CONFIRMADOS

| ID | Versión revisada verificable | Trazabilidad | Observación / límite |
|---|---|---|---|
| CA-JOR-01 | El estado efectivo de la jornada en el ciclo ordinario pertenece exclusivamente a SIN_ABRIR, ABIERTA o CERRADA. | DEC-01/DEC-03, aprobación catálogo PO. | No añade estados para descanso, regularización o corrección. |
| CA-JOR-02 | Antes de abrir manualmente, la jornada es SIN_ABRIR, aun si tiene compromisos programados. | DEC-01; RN-01; RF-011. | No autoriza todavía asignaciones futuras ni ejecución antes de apertura. |
| CA-JOR-03 | La apertura manual cambia SIN_ABRIR a ABIERTA conservando los compromisos asociados. | DEC-01; RN-01; RF-011. | No introduce apertura automática por trabajo o paso del tiempo. |
| CA-JOR-04 | Abrir no resuelve ni modifica automáticamente planificación, estado o resolución de compromisos ya asociados. | DEC-01; RN-01; FR-3, independencia aprobada en DEC-62 como antecedente. | Precisión propuesta; no se aprueba por inferencia. |
| CA-JOR-05 | ABIERTA permite las operaciones de planificación, registro de avances y resolución previamente aprobadas, bajo sus condiciones y límites. | RF-010/RF-011/RF-016/RF-025; RN-02/RN-04; FR-1 a FR-4. | No habilita todas las acciones/transiciones posibles. |
| CA-JOR-06 | Si algún compromiso de la jornada permanece PENDIENTE, no se permite confirmar el cierre. | RF-025; RN-03; DEC-03. | Decisiones meramente preparadas no son resoluciones efectivas fuera del proceso específico aprobado de cancelación definitiva. No se generaliza ese mecanismo al cierre diario. |
| CA-JOR-07 | Resolver todos los compromisos no cierra la jornada: permanece ABIERTA hasta confirmación manual. | RF-025; RN-03; DEC-03, precisión PO. | No decide tratamiento de jornadas SIN_ABRIR con compromisos resueltos. |
| CA-JOR-08 | La confirmación manual válida de cierre de una jornada ABIERTA cambia su estado a CERRADA y conserva registro del cierre. | RF-025; RN-03; DEC-03. | Datos exactos de registro pendientes; no prescribe almacenamiento. |
| CA-JOR-09 | Una jornada ABIERTA sin compromisos puede cerrarse mediante confirmación manual sin que esa ausencia cuente como incumplimiento. | DEC-64, precisión PO; RF-025/RN-03. | Fórmulas pendientes; cierre directo desde SIN_ABRIR prohibido por precisión posterior del PO. |
| CA-JOR-10 | Al confirmar válidamente un día de descanso, la jornada resultante es CERRADA y queda identificada explícitamente como descanso. | RF-015; RN-23; DEC-23, precisión PO. | La precisión posterior del PO exige abrir primero. |
| CA-JOR-11 | Antes de confirmar descanso deben estar resueltos los compromisos asumidos, incluido traslado por reprogramación con categoría, explicación y fecha destino cuando corresponda. | RF-015/RF-026/RF-027; RN-23/RN-04 a RN-06; DEC-23. | No altera historial ni considera el traslado cumplimiento. |
| CA-JOR-12 | La declaración de descanso no genera por sí misma una penalización de cumplimiento. | RF-015; RN-23; DEC-23. | No elimina compromisos asumidos ni define denominadores: DEC-63 pendiente. |
| CA-JOR-13 | Una fecha pasada con compromisos asumidos y sin cierre confirmado se identifica para regularización aunque la jornada sea SIN_ABRIR. | RF-028; RN-08; DEC-08, precisión PO. | Fecha pasada según calendario del usuario; zona inicial America/Santiago/RN-24. Corte por medianoche pendiente DEC-68. |
| CA-JOR-14 | Cada jornada histórica se regulariza individualmente conservando su fecha original; los avances mantienen su fecha real. | RF-028/RF-017; RN-08/RN-16; DEC-08/DEC-16. | No traslada trabajo real al día original por regularizar. |
| CA-JOR-15 | La regularización resuelve los compromisos pendientes y requiere confirmación manual del cierre; resolverlos no cierra automáticamente. | RF-028/RF-025; RN-08/RN-03 a RN-06; DEC-08/DEC-03. | Precisión posterior confirmada: apertura manual previa obligatoria. |
| CA-JOR-16 | Corregir una jornada CERRADA exige justificación y auditoría, manteniéndola CERRADA sin reapertura. | RF-028; RN-20; DEC-20/DEC-69. | Alcance y transiciones de resoluciones históricas siguen pendientes. |
| CA-JOR-17 | Correcciones históricas aprobadas actualizan estadísticas actuales y conservan revisiones originales e historial. | RF-032; RN-28; DEC-28/DEC-69. | No permite correcciones arbitrarias ni altera revisiones originales. |

## Itinerario obligatorio — CONFIRMADO por el PO

Único ciclo ordinario SIN_ABRIR → ABIERTA → CERRADA. Todas las jornadas deben abrirse manualmente antes de poder cerrarse, incluidas históricas, vacías y descansos. No hay cierre directo desde SIN_ABRIR. Una histórica SIN_ABRIR se abre manualmente para regularización conservando fecha original; una vacía se abre y luego puede cerrarse sin penalización. Para declarar descanso debe estar ABIERTA y sus compromisos deben estar resueltos o trasladados justificadamente antes de confirmar descanso y cierre.

La misma interfaz puede simplificar la experiencia, conservando confirmaciones de apertura y cierre como operaciones lógicas independientes. La fecha de la jornada se distingue del momento real de apertura/cierre. Una corrección mantiene CERRADA sin reapertura. Se registran precisiones bajo DEC-01/DEC-03/DEC-08/DEC-23/DEC-64 y vínculo RN-20/DEC-20; sin nuevos IDs de decisión ni mecanismos técnicos.

Pendiente de apertura describe SIN_ABRIR; pendiente de cierre describe ABIERTA sin cierre confirmado. No son estados adicionales. Resolver todos los compromisos no cierra automáticamente. Una fecha histórica con compromisos asumidos y sin cierre requiere regularización individual, incluso nunca abierta. No se aprueba automáticamente otra conducta de jornadas pasadas vacías nunca abiertas.

## CA-JOR-18 a CA-JOR-25 — CONFIRMADOS

| ID | Criterio verificable | Estado | Trazabilidad |
|---|---|---|---|
| CA-JOR-18 | Toda jornada que se cierra ha pasado previamente por apertura manual, incluidas históricas, vacías y descansos; el ciclo ordinario es SIN_ABRIR → ABIERTA → CERRADA. | CONFIRMADO | DEC-01/DEC-03; RN-01/RN-03; CA-JOR-01/03/08. |
| CA-JOR-19 | Si una jornada está SIN_ABRIR, no se permite confirmar directamente su cierre; debe abrirse manualmente primero. | CONFIRMADO | DEC-01/DEC-03; RN-01; CA-JOR-03/08. |
| CA-JOR-20 | Para regularizar una histórica SIN_ABRIR con compromisos asumidos, se abre manualmente en su fecha original, se resuelven sus compromisos y se confirma cierre; la apertura posterior no cambia esa fecha. | CONFIRMADO | DEC-08; RF-028; RN-08; CA-JOR-13/14/15. |
| CA-JOR-21 | Una jornada sin compromisos puede abrirse y cerrarse manualmente sin que la ausencia de compromisos se contabilice como incumplimiento. No define fórmulas ni tratamiento de días nunca abiertos. | CONFIRMADO | DEC-64; CA-JOR-09; RF-025. |
| CA-JOR-22 | Solo una jornada ABIERTA permite confirmar descanso y cierre; sus compromisos deben estar resueltos o trasladados justificadamente. El resultado es CERRADA e identificado como descanso. | CONFIRMADO | DEC-23; RF-015; RN-23; CA-JOR-10/11/12. |
| CA-JOR-23 | Si apertura y cierre se ofrecen en una misma interfaz, conservan dos confirmaciones manuales lógicamente independientes; confirmar apertura no confirma por sí mismo cierre ni descanso. | CONFIRMADO | DEC-01/DEC-03/DEC-23; RN-01/RN-03; nueva precisión PO. |
| CA-JOR-24 | Puede distinguirse la fecha de la jornada del momento real de su apertura y cierre, incluso al regularizar una fecha pasada; no se registra la apertura o cierre como si hubieran ocurrido en la fecha histórica. No prescribe formato, precisión temporal ni almacenamiento. | CONFIRMADO | DEC-08; RN-08; nueva precisión PO; DEC-68 pendiente. |
| CA-JOR-25 | Una corrección justificada y auditada de CERRADA no ejecuta apertura ni la cambia a ABIERTA; mantiene CERRADA conservando historial. | CONFIRMADO | DEC-20; RN-20; CA-JOR-16/17; DEC-69 pendiente. |

## Pendientes conservados

DEC-60 resuelta para planificar en SIN_ABRIR y registrar avances/confirmar cumplimiento solo en ABIERTA; criterios CA-DEC60-01 a CA-DEC60-04 aprobados e incorporados en FR-6. Permanecen pendientes: cierre anticipado y actividades posteriores (DEC-61); días pasados sin compromisos y nunca abiertos (DEC-64 parcial); fórmulas de jornadas vacías/descansos (DEC-63); alcance de correcciones históricas (DEC-69); jornadas abiertas simultáneamente; medianoche/zona horaria (DEC-68). También siguen abiertos creación/reconocimiento de jornadas, modificación/revocación de descanso y conflictos entre períodos DEC-73.

CA-JOR-18 a CA-JOR-25 fueron aprobados explícitamente por el PO e incorporados como CONFIRMADOS al borrador. No se amplía DEC-62 ni se generan implementación o historias. PRD draft.

## Excepción posterior CONFIRMADA — DEC-61

El PO autoriza reapertura explícita justificada CERRADA → ABIERTA para ingresar otra actividad del mismo día. El ciclo ordinario conserva sus estados y transiciones; la prohibición absoluta de reapertura queda sustituida por esta excepción. Corregir auditadamente no reabre por sí mismo (CA-JOR-16/25). Criterios CA-DEC61-01 a CA-DEC61-04 aprobados y pendientes restantes en [DEC-61](decision-dec-61.md). No se modifican silenciosamente criterios previamente aprobados.

## Precisión posterior de zona horaria — DEC-68 CONFIRMADA

Zona reportada por navegador sustituye America/Santiago fija de DEC-24/RN-24. Día local cambia a medianoche. Semana sigue desde lunes. No se modifican silenciosamente fuentes históricas ni criterios; la precisión prevalece para fecha actual del usuario. Cambios de zona, sesiones que cruzan medianoche y fallback siguen pendientes. Véase [DEC-68](decision-dec-68.md).

## Precisión posterior DEC-64 — CONFIRMADA

Fecha pasada nunca abierta y sin compromisos asumidos no exige regularización ni se considera incumplimiento automáticamente. No equivale a fecha que tuvo compromisos luego resueltos/retirados; no modifica estados automáticamente. Pendientes vacías abiertas sin cierre y fórmulas. CA-DEC64-01 a CA-DEC64-04 CONFIRMADOS en [DEC-64](decision-dec-64.md) e incorporados en FR-9.

## Jornadas abiertas simultáneamente — CONFIRMADO

El PO acepta permitir abrir manualmente la jornada actual aunque existan jornadas anteriores ABIERTAS. La apertura actual no cierra ni modifica automáticamente las anteriores; cada jornada conserva fecha, compromisos y obligación de cierre individual. Las anteriores bloquean confirmación de cierre de sus revisiones periódicas según DEC-27/RN-27 ampliada. Se registra precisión bajo DEC-01/DEC-08/DEC-27 existentes, sin nuevo ID de decisión ni estado.

Esta aprobación se limita a jornadas de fechas distintas y no resuelve compromisos duplicados, registros de varias jornadas para una misma fecha ni asignaciones futuras.

### CA-JOR-26 a CA-JOR-28 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-JOR-26 | La presencia de jornadas anteriores ABIERTAS no impide abrir manualmente la jornada actual bajo las demás condiciones aprobadas. | DEC-01/DEC-08, nueva aprobación PO; CA-JOR-03; FR-6/FR-8. |
| CA-JOR-27 | Abrir la jornada actual no cierra ni modifica automáticamente estado, fecha o compromisos de jornadas anteriores abiertas. | DEC-01/DEC-08; RN-08; CA-JOR-07/14. |
| CA-JOR-28 | Cada jornada anterior abierta conserva obligación de cierre manual individual y bloquea la confirmación del cierre de su revisión periódica correspondiente mientras siga abierta. | DEC-08/DEC-27; CA-DEC27-01/02; CA-DEC64-06. |

CA-JOR-26 a CA-JOR-28 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Fecha/zonas y atribución real de avances conservan sus reglas previas. Duplicados y futuras siguen pendientes. PRD draft.
