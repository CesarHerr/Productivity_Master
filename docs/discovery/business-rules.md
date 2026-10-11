# Reglas de negocio — Productivity_Master

**Fecha:** 2026-10-11 · **Estado documental:** consolidado para revisión, no autorización de implementación.

## Lectura del catálogo

Los términos tarea, compromiso, ejecución y registro de avance se usan provisionalmente como en el descubrimiento; su definición exacta es **PENDIENTE** ([DEC-62](decision-log.md#dec-62)). Este documento no define modelos técnicos.

RN-01 a RN-14 conservan los identificadores del original. RN-15 a RN-29 no tenían definiciones disponibles en el repositorio: las asignaciones siguientes son incorporaciones explícitas basadas en confirmaciones del PO, no una reconstrucción de un catálogo previo. Las diferencias están registradas en [decision-log.md](decision-log.md#diferencias-respecto-del-original).

## Catálogo RN-01 a RN-29

<a id="rn-01"></a>

### RN-01 — Apertura manual

**Estado:** CONFIRMADO · **Fuente:** Original RN-01 + PO.

La jornada se abre manualmente.

**Decisión:** [DEC-01](decision-log.md#dec-01). **Requisitos:** [RF-011](requirements-baseline.md#rf-011). **Pendientes/dependencias:** [DEC-60](decision-log.md#dec-60).

<a id="rn-02"></a>

### RN-02 — Edición durante la jornada

**Estado:** CONFIRMADO · **Fuente:** Original RN-02 + PO.

Las actividades planificadas pueden editarse mientras la jornada permanezca abierta; conservar el compromiso original y registrar cambios según [RN-18](business-rules.md#rn-18).

**Decisión:** [DEC-02](decision-log.md#dec-02). **Requisitos:** [RF-010](requirements-baseline.md#rf-010), [RF-011](requirements-baseline.md#rf-011). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62).

<a id="rn-03"></a>

### RN-03 — Cierre con resolución completa

**Estado:** CONFIRMADO · **Fuente:** Original RN-03 + PO.

El cierre diario es manual y no puede confirmarse mientras existan compromisos sin resolver.

**Decisión:** [DEC-03](decision-log.md#dec-03). **Requisitos:** [RF-025](requirements-baseline.md#rf-025). **Pendientes/dependencias:** [DEC-61](decision-log.md#dec-61), [DEC-64](decision-log.md#dec-64).

<a id="rn-04"></a>

### RN-04 — Resolución de compromisos

**Estado:** CONFIRMADO · **Fuente:** Original RN-04 + PO.

Los compromisos pendientes se resuelven mediante cumplimiento, cancelación o reprogramación.

**Decisión:** [DEC-04](decision-log.md#dec-04). **Requisitos:** [RF-025](requirements-baseline.md#rf-025). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-66](decision-log.md#dec-66).

<a id="rn-05"></a>

### RN-05 — Justificación obligatoria

**Estado:** CONFIRMADO · **Fuente:** Original RN-05 + PO.

Cancelar o reprogramar exige seleccionar una categoría y escribir una explicación textual obligatoria.

**Decisión:** [DEC-05](decision-log.md#dec-05). **Requisitos:** [RF-026](requirements-baseline.md#rf-026). **Pendientes/dependencias:** [DEC-65](decision-log.md#dec-65).

<a id="rn-06"></a>

### RN-06 — Fecha de destino

**Estado:** CONFIRMADO · **Fuente:** Original RN-06 + PO.

Reprogramar requiere una fecha de destino.

**Decisión:** [DEC-06](decision-log.md#dec-06). **Requisitos:** [RF-027](requirements-baseline.md#rf-027). **Pendientes/dependencias:** [DEC-67](decision-log.md#dec-67).

<a id="rn-07"></a>

### RN-07 — Progreso conservado

**Estado:** CONFIRMADO · **Fuente:** Original RN-07 + PO.

Se conservan los avances parciales, también al reprogramar una tarea.

**Decisión:** [DEC-07](decision-log.md#dec-07). **Requisitos:** [RF-017](requirements-baseline.md#rf-017), [RF-027](requirements-baseline.md#rf-027). **Pendientes/dependencias:** [DEC-68](decision-log.md#dec-68).

<a id="rn-08"></a>

### RN-08 — Regularización individual

**Estado:** CONFIRMADO · **Fuente:** Original RN-08 + PO.

Las jornadas antiguas pendientes se regularizan individualmente y conservan sus fechas originales; los avances mantienen su fecha real según [RN-16](business-rules.md#rn-16).

**Decisión:** [DEC-08](decision-log.md#dec-08). **Requisitos:** [RF-028](requirements-baseline.md#rf-028). **Pendientes/dependencias:** [DEC-69](decision-log.md#dec-69).

<a id="rn-09"></a>

### RN-09 — Hábitos incumplidos

**Estado:** CONFIRMADO · **Fuente:** Original RN-09 + PO.

Las sesiones incumplidas pueden justificarse o recuperarse en otra fecha; [RN-21](business-rules.md#rn-21) exige conservar el incumplimiento histórico.

**Decisión:** [DEC-09](decision-log.md#dec-09). **Requisitos:** [RF-022](requirements-baseline.md#rf-022). **Pendientes/dependencias:** [DEC-66](decision-log.md#dec-66), [DEC-67](decision-log.md#dec-67).

<a id="rn-10"></a>

### RN-10 — Revisión periódica

**Estado:** CONFIRMADO · **Fuente:** Original RN-10 + PO.

Los cierres semanales y mensuales son manuales e incorporan resumen automático, reflexiones y definición de próximos compromisos.

**Decisión:** [DEC-10](decision-log.md#dec-10). **Requisitos:** [RF-008](requirements-baseline.md#rf-008), [RF-029](requirements-baseline.md#rf-029). **Pendientes/dependencias:** [DEC-73](decision-log.md#dec-73).

<a id="rn-11"></a>

### RN-11 — Historial de reprogramación

**Estado:** CONFIRMADO · **Fuente:** Original RN-11 (propuesta) + PO.

La reprogramación conserva el compromiso original en el historial y no lo convierte en completado. Las correcciones históricas siguen [RN-20](business-rules.md#rn-20) y [RN-28](business-rules.md#rn-28).

**Decisión:** [DEC-11](decision-log.md#dec-11). **Requisitos:** [RF-027](requirements-baseline.md#rf-027), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-69](decision-log.md#dec-69).

<a id="rn-12"></a>

### RN-12 — Integridad operativa

**Estado:** PROPUESTO · **Fuente:** Original RN-12 y §6 M7.

Proteger cierres y reprogramaciones contra actualizaciones parciales y conflictos concurrentes, mediante operaciones transaccionales u otros mecanismos por validar. Evitar duplicados sí está confirmado en [RN-26](business-rules.md#rn-26).

**Decisión:** [DEC-12](decision-log.md#dec-12). **Requisitos:** [RNF-003](requirements-baseline.md#rnf-003). **Pendientes/dependencias:** [DEC-70](decision-log.md#dec-70).

<a id="rn-13"></a>

### RN-13 — Autorización

**Estado:** PROPUESTO · **Fuente:** Original RN-13.

Asociar recursos personales a un usuario y sujetarlos a autorización de acceso. El aislamiento es propuesto; autenticación y estrategia concreta siguen pendientes.

**Decisión:** [DEC-13](decision-log.md#dec-13). **Requisitos:** [RF-003](requirements-baseline.md#rf-003), [RNF-004](requirements-baseline.md#rnf-004). **Pendientes/dependencias:** [DEC-70](decision-log.md#dec-70).

<a id="rn-14"></a>

### RN-14 — Ejecuciones recurrentes

**Estado:** PROPUESTO · **Fuente:** Original RN-14.

Cada ejecución recurrente tendría estado e historial propios; reprogramar una ejecución no alteraría las siguientes ocurrencias de la serie. Frecuencia futura y recuperación histórica sí están confirmadas en [RN-22](business-rules.md#rn-22) y [RN-21](business-rules.md#rn-21).

**Decisión:** [DEC-14](decision-log.md#dec-14). **Requisitos:** [RF-024](requirements-baseline.md#rf-024). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-67](decision-log.md#dec-67).

<a id="rn-15"></a>

### RN-15 — Cumplimiento explícito

**Estado:** CONFIRMADO · **Fuente:** PO.

Una tarea solo se completa mediante confirmación explícita, incluso si su métrica alcanza el 100 %.

**Decisión:** [DEC-15](decision-log.md#dec-15). **Requisitos:** [RF-016](requirements-baseline.md#rf-016), [RF-018](requirements-baseline.md#rf-018). **Pendientes/dependencias:** [DEC-74](decision-log.md#dec-74).

<a id="rn-16"></a>

### RN-16 — Fecha real del avance

**Estado:** CONFIRMADO · **Fuente:** PO.

Los avances pertenecen a su fecha real de ejecución. La atribución del trabajo después de medianoche sigue pendiente.

**Decisión:** [DEC-16](decision-log.md#dec-16). **Requisitos:** [RF-017](requirements-baseline.md#rf-017), [RF-020](requirements-baseline.md#rf-020), [RF-034](requirements-baseline.md#rf-034). **Pendientes/dependencias:** [DEC-68](decision-log.md#dec-68).

<a id="rn-17"></a>

### RN-17 — Tres dimensiones del seguimiento

**Estado:** CONFIRMADO · **Fuente:** PO.

Distinguir cumplimiento, esfuerzo realizado y avance hacia objetivos; separar el registro del trabajo de su resultado de cumplimiento.

**Decisión:** [DEC-17](decision-log.md#dec-17). **Requisitos:** [RF-006](requirements-baseline.md#rf-006), [RF-016](requirements-baseline.md#rf-016), [RF-019](requirements-baseline.md#rf-019), [RF-020](requirements-baseline.md#rf-020), [RF-033](requirements-baseline.md#rf-033), [RF-034](requirements-baseline.md#rf-034), [RF-036](requirements-baseline.md#rf-036). **Pendientes/dependencias:** [DEC-63](decision-log.md#dec-63), [DEC-74](decision-log.md#dec-74).

<a id="rn-18"></a>

### RN-18 — Edición trazable

**Estado:** CONFIRMADO · **Fuente:** PO.

Editar una tarea conserva el compromiso original y registra los cambios.

**Decisión:** [DEC-18](decision-log.md#dec-18). **Requisitos:** [RF-010](requirements-baseline.md#rf-010), [RF-012](requirements-baseline.md#rf-012), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62).

<a id="rn-19"></a>

### RN-19 — Retiro del día

**Estado:** CONFIRMADO · **Fuente:** PO.

Retirar una tarea del día exige justificación, conserva el compromiso en el historial y no lo excluye del conjunto de compromisos asumidos para el cumplimiento. Su correspondencia con cancelación o reprogramación sigue pendiente.

**Decisión:** [DEC-19](decision-log.md#dec-19). **Requisitos:** [RF-013](requirements-baseline.md#rf-013), [RF-035](requirements-baseline.md#rf-035), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-63](decision-log.md#dec-63).

<a id="rn-20"></a>

### RN-20 — Corrección sin reapertura

**Estado:** CONFIRMADO · **Fuente:** PO.

Las correcciones de jornadas cerradas requieren justificación y auditoría, sin reabrirlas. El alcance permitido de la corrección sigue pendiente.

**Decisión:** [DEC-20](decision-log.md#dec-20). **Requisitos:** [RF-028](requirements-baseline.md#rf-028), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-69](decision-log.md#dec-69).

<a id="rn-21"></a>

### RN-21 — Recuperación separada

**Estado:** CONFIRMADO · **Fuente:** PO.

La recuperación de una sesión se registra separadamente y no elimina el incumplimiento histórico original.

**Decisión:** [DEC-21](decision-log.md#dec-21). **Requisitos:** [RF-022](requirements-baseline.md#rf-022), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-66](decision-log.md#dec-66), [DEC-67](decision-log.md#dec-67).

<a id="rn-22"></a>

### RN-22 — Cambio de frecuencia

**Estado:** CONFIRMADO · **Fuente:** PO.

Cambiar la frecuencia de un hábito o tarea recurrente solo afecta sesiones futuras. El corte temporal exacto para sesiones futuras queda pendiente.

**Decisión:** [DEC-22](decision-log.md#dec-22). **Requisitos:** [RF-023](requirements-baseline.md#rf-023). **Pendientes/dependencias:** [DEC-75](decision-log.md#dec-75).

<a id="rn-23"></a>

### RN-23 — Descansos

**Estado:** CONFIRMADO · **Fuente:** PO.

El usuario puede declarar días de descanso; no perjudican las estadísticas de cumplimiento. Si existen compromisos asumidos, deben resolverse o trasladarse justificadamente antes de confirmar el descanso. La fórmula que concilia descanso y compromisos históricos sigue pendiente.

**Decisión:** [DEC-23](decision-log.md#dec-23). **Requisitos:** [RF-015](requirements-baseline.md#rf-015). **Pendientes/dependencias:** [DEC-63](decision-log.md#dec-63), [DEC-64](decision-log.md#dec-64).

<a id="rn-24"></a>

### RN-24 — Calendario inicial

**Estado:** CONFIRMADO · **Fuente:** PO.

La semana comienza el lunes y la zona horaria inicial es America/Santiago. Se contempla personalización futura; su alcance y momento no están definidos.

**Decisión:** [DEC-24](decision-log.md#dec-24). **Requisitos:** [RF-002](requirements-baseline.md#rf-002), [RF-008](requirements-baseline.md#rf-008). **Pendientes/dependencias:** [DEC-68](decision-log.md#dec-68), [DEC-72](decision-log.md#dec-72).

<a id="rn-25"></a>

### RN-25 — Compromisos que cuentan

**Estado:** CONFIRMADO · **Fuente:** PO.

Todos los compromisos asumidos durante la jornada cuentan para el cumplimiento, incluidos los retirados justificadamente. Una tarea no planificada inicialmente puede contar si fue incorporada formalmente. Cancelados y reprogramados no cuentan como completados. Las fórmulas finales siguen pendientes.

**Decisión:** [DEC-25](decision-log.md#dec-25). **Requisitos:** [RF-013](requirements-baseline.md#rf-013), [RF-035](requirements-baseline.md#rf-035). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-63](decision-log.md#dec-63).

<a id="rn-26"></a>

### RN-26 — Sin doble contabilización

**Estado:** CONFIRMADO · **Fuente:** PO.

Evitar contabilizaciones duplicadas de ejecuciones o progreso. No se confirma un mecanismo técnico ni una fórmula de agregación.

**Decisión:** [DEC-26](decision-log.md#dec-26). **Requisitos:** [RF-019](requirements-baseline.md#rf-019), [RF-034](requirements-baseline.md#rf-034), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-63](decision-log.md#dec-63), [DEC-67](decision-log.md#dec-67).

<a id="rn-27"></a>

### RN-27 — Condición del cierre periódico

**Estado:** CONFIRMADO · **Fuente:** PO.

No se permite cerrar una revisión semanal o mensual si existen jornadas comprometidas pendientes de regularización en el período revisado. La definición exacta de jornada comprometida sigue pendiente.

**Decisión:** [DEC-27](decision-log.md#dec-27). **Requisitos:** [RF-031](requirements-baseline.md#rf-031). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-73](decision-log.md#dec-73).

<a id="rn-28"></a>

### RN-28 — Correcciones y revisiones originales

**Estado:** CONFIRMADO · **Fuente:** PO.

Las correcciones históricas actualizan las estadísticas actuales, pero conservan las revisiones originales y su historial.

**Decisión:** [DEC-28](decision-log.md#dec-28). **Requisitos:** [RF-032](requirements-baseline.md#rf-032), [RNF-002](requirements-baseline.md#rnf-002). **Pendientes/dependencias:** [DEC-69](decision-log.md#dec-69).

<a id="rn-29"></a>

### RN-29 — Archivo de objetivos

**Estado:** CONFIRMADO · **Fuente:** PO.

No puede archivarse un objetivo con tareas activas sin antes resolverlas o reasignarlas. La definición de tarea activa y el archivo de hitos siguen pendientes.

**Decisión:** [DEC-29](decision-log.md#dec-29). **Requisitos:** [RF-005](requirements-baseline.md#rf-005), [RF-007](requirements-baseline.md#rf-007). **Pendientes/dependencias:** [DEC-62](decision-log.md#dec-62), [DEC-71](decision-log.md#dec-71).

## Estados y transiciones conceptuales

| Objeto provisional | Transición confirmada | Condición o límite |
|---|---|---|
| Jornada | Apertura manual; abierta → cerrada por cierre manual | [RN-01](business-rules.md#rn-01) y [RN-03](business-rules.md#rn-03); todos los compromisos resueltos. No se fija estado previo ni cantidad de jornadas abiertas. |
| Compromiso pendiente | Resolución por cumplimiento, cancelación o reprogramación | [RN-04](business-rules.md#rn-04) a [RN-06](business-rules.md#rn-06) y [RN-15](business-rules.md#rn-15). No equivale a definir estados de la tarea persistente. |
| Jornada cerrada | Corrección justificada y auditada manteniendo cierre | [RN-20](business-rules.md#rn-20); sin reapertura. Campos corregibles pendientes. |
| Sesión incumplida | Puede justificarse o recuperarse separadamente | [RN-09](business-rules.md#rn-09) y [RN-21](business-rules.md#rn-21); recuperación no borra incumplimiento. No se define un estado nuevo obligatorio. |
| Objetivo con tareas activas | Archivo solo después de resolverlas o reasignarlas | [RN-29](business-rules.md#rn-29); significado exacto de tarea activa pendiente. |

**Invariantes del cierre diario:** cierre manual; ausencia de compromisos sin resolver; cumplimiento explícito; categoría y texto para cancelación/reprogramación; fecha destino para reprogramación; avances parciales y compromiso original conservados. Un retiro no borra el compromiso ni lo elimina del conjunto que cuenta. El mapeo retiro → resolución permanece pendiente.

**Invariantes históricos:** fecha original de jornada conservada; avances en fecha real; recuperación independiente; corrección auditada sin reapertura; estadísticas actuales corregibles y revisiones originales preservadas. No confundir conservación del original con prohibición total de correcciones.

## Indicadores preliminares

Todos los indicadores y las expresiones de la fuente son **PROPUESTOS**; fórmulas finales y denominadores son **PENDIENTES** ([DEC-43](decision-log.md#dec-43), [DEC-63](decision-log.md#dec-63)). La inclusión de compromisos asumidos, la separación de dimensiones, la ausencia de doble conteo y el tratamiento de descansos sí están confirmados ([RN-17](business-rules.md#rn-17), [RN-23](business-rules.md#rn-23), [RN-25](business-rules.md#rn-25), [RN-26](business-rules.md#rn-26)).

| Indicador | Definición preliminar conservada de §9 original — PROPUESTO | Detalle PENDIENTE |
|---|---|---|
| Cumplimiento diario | Ejecuciones completadas / ejecuciones comprometidas | Identidad de ejecución, incorporación formal, retiros y descanso con compromisos. |
| Cumplimiento semanal | Ejecuciones completadas / comprometidas durante la semana | Compromisos propios y traslados entre períodos; semana comienza lunes. |
| Cumplimiento mensual | Ejecuciones completadas / comprometidas durante el mes | Relación con compromisos diarios/semanales y atribución de cumplimiento. |
| Tiempo realizado | Suma del tiempo de ejecución registrado | Correcciones, sesiones solapadas, medianoche y evitar duplicados. |
| Adherencia a hábitos | Sesiones cumplidas / sesiones previstas | Recuperaciones, pausas y cambios de frecuencia; no borrar incumplimiento original. |
| Reprogramaciones | Cantidad de ejecuciones reprogramadas | Eventos sucesivos frente a compromisos únicos. |
| Cancelaciones | Cantidad de ejecuciones canceladas | Correspondencia de retiro con cancelación. |
| Consistencia | Jornadas cerradas / jornadas esperadas | Descansos y jornadas vacías. |
| Avance de objetivos | Valor ejecutado respecto de meta definida | Unidades, contribuciones, objetivos sin métrica y esfuerzo frente a resultado. |

El trabajo registrado se conserva independientemente del cumplimiento. Cancelar o reprogramar no cuenta como completar. No sumar directamente tiempo, cantidad y porcentaje como si fueran una sola magnitud; la agregación concreta sigue pendiente, no se prescribe una fórmula.

## Ejemplos de aplicación y límites

Los ejemplos ilustran reglas; no agregan decisiones.

1. **Caso normal:** con jornada abierta, registrar 35 minutos en una tarea estimada en 45 y confirmar explícitamente su cumplimiento. La duración estimada es opcional; no define por sí sola una condición de completado ([RN-15](business-rules.md#rn-15), [DEC-36](decision-log.md#dec-36), [DEC-74](decision-log.md#dec-74)).
2. **Meta al 100 %:** registrar 100 % no completa automáticamente. Si no hay confirmación ni otra resolución, el compromiso sigue sin resolver y bloquea cierre ([RN-03](business-rules.md#rn-03), [RN-15](business-rules.md#rn-15)).
3. **Avance parcial y traslado:** el lunes registrar 35 minutos y reprogramar al martes con categoría y explicación. El compromiso del lunes queda resuelto por reprogramación, no completado; los 35 minutos siguen en lunes. Trabajo real del martes pertenece al martes. Evitar contar el avance previo otra vez ([RN-06](business-rules.md#rn-06), [RN-07](business-rules.md#rn-07), [RN-11](business-rules.md#rn-11), [RN-16](business-rules.md#rn-16), [RN-26](business-rules.md#rn-26)).
4. **Retiro después de apertura:** retirar una tarea requiere justificación y conserva su compromiso en historial y conjunto de cumplimiento. No se declara que el retiro sea un cuarto estado de resolución: su encaje con [RN-04](business-rules.md#rn-04) es PENDIENTE ([RN-19](business-rules.md#rn-19), [RN-25](business-rules.md#rn-25), [DEC-62](decision-log.md#dec-62)).
5. **Recuperación de hábito:** sesión incumplida el lunes y recuperación el miércoles. El incumplimiento del lunes permanece y la recuperación se registra separadamente. Si ya había sesión el miércoles, la coexistencia o sustitución está PENDIENTE ([RN-21](business-rules.md#rn-21), [DEC-67](decision-log.md#dec-67)).
6. **Descanso con compromisos:** antes de confirmar descanso, resolver o trasladar justificadamente los compromisos. Descanso no perjudica cumplimiento; cómo representar ese día en las fórmulas sin borrar compromisos es PENDIENTE ([RN-23](business-rules.md#rn-23), [RN-25](business-rules.md#rn-25), [DEC-63](decision-log.md#dec-63)).
7. **Revisión bloqueada:** una jornada comprometida pendiente de regularización impide cerrar la revisión del período; regularizarla conserva su fecha original. Clasificación exacta de jornada comprometida y conflictos entre períodos: PENDIENTES ([RN-08](business-rules.md#rn-08), [RN-27](business-rules.md#rn-27), [DEC-62](decision-log.md#dec-62), [DEC-73](decision-log.md#dec-73)).
8. **Corrección después de revisión:** corregir justificadamente una jornada cerrada sin reabrir; estadísticas actuales cambian y revisión original conserva contenido e historial. Campos y límites de corrección: PENDIENTES ([RN-20](business-rules.md#rn-20), [RN-28](business-rules.md#rn-28), [DEC-69](decision-log.md#dec-69)).
9. **Cambio de frecuencia:** cambiar de diaria a días seleccionados afecta solo sesiones futuras. Qué hacer con sesiones futuras ya generadas es PENDIENTE ([RN-22](business-rules.md#rn-22), [DEC-75](decision-log.md#dec-75)).
10. **Archivo:** objetivo con tareas activas no se archiva hasta resolverlas o reasignarlas. No extrapolar esta regla a hitos: su tratamiento está PENDIENTE ([RN-29](business-rules.md#rn-29), [DEC-71](decision-log.md#dec-71)).
11. **Jerarquía y unidades:** Desarrollo profesional → Mejorar inglés → Completar 20 sesiones → Practicar 45 minutos; registrar 35 minutos no demuestra por sí solo haber ganado una sesión del hito. Contribución al resultado: PENDIENTE ([DEC-31](decision-log.md#dec-31), [DEC-74](decision-log.md#dec-74)).
12. **Medianoche o actividad posterior al cierre:** la fecha real está confirmada y no se reabre la jornada; la atribución después de medianoche y el registro posterior al cierre siguen PENDIENTES. No se prescribe traslado automático ([RN-16](business-rules.md#rn-16), [RN-20](business-rules.md#rn-20), [DEC-61](decision-log.md#dec-61), [DEC-68](decision-log.md#dec-68)).

## Flujos originales preservados

Los flujos A–E de §8 se mantienen como orientación conceptual, no como aprobación de cada detalle de interfaz:

- **A — Inicio:** ingresar, visualizar compromisos/hábitos/pendientes, revisar planificación, abrir manualmente, agregar/modificar o priorizar y comenzar. Priorizar y la vista específica son PROPUESTOS; registro antes de apertura PENDIENTE.
- **B — Trabajo:** seleccionar actividad, registrar avances o notas, consultar progreso, confirmar cumplimiento o mantener pendiente y continuar. Notas son PROPUESTAS; alcanzar meta no completa automáticamente.
- **C — Cierre:** solicitar, revisar pendientes, confirmar cumplimiento o justificar cancelación/reprogramación, definir destino, verificar resolución completa, reflexión opcional y confirmar con historial. Revisión de interfaz y reflexión diaria son PROPUESTAS.
- **D — Regularización:** detectar jornadas sin cierre, mostrar fechas/compromisos, regularizar cada fecha, registrar resultados/justificaciones y cerrar individualmente. La jornada conserva fecha original y cada avance fecha real.
- **E — Revisión:** seleccionar período, revisar resumen, consultar cumplimiento/avance, identificar causas, reflexionar, planificar próximos compromisos y cerrar. Consulta detallada/causas son PROPUESTAS; [RN-27](business-rules.md#rn-27) condiciona cierre.
