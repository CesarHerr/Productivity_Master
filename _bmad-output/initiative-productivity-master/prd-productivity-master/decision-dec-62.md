# DEC-62 — Resolución parcial y criterios aprobados

**Fecha:** 2026-10-11. **Origen:** aprobación explícita del Product Owner en la conversación de elaboración del PRD.

**Estado de la decisión descrita:** CONFIRMADO. **Estado de los criterios CA-DEC62-01 a CA-DEC62-09:** CONFIRMADO por aprobación explícita del PO; incorporados al borrador del PRD. **DEC-62 en su conjunto:** parcialmente resuelta; no se declara cerrada.

Esta nota documenta la aprobación posterior al [registro de descubrimiento](../../../docs/discovery/decision-log.md#dec-62). No modifica las fuentes aprobadas. Los nueve criterios aprobados se incorporan al borrador del PRD, que permanece abierto.

## Comportamiento aprobado

- Una tarea mantiene su identidad a través de los días, independientemente de cuántas veces se reprograme.
- Cada fecha en que se asume realizarla tiene un compromiso diario propio, con planificación, estado y resolución independientes.
- Los registros de avance representan trabajo realmente realizado y pertenecen a su fecha de ejecución.
- La aplicación mantiene trazabilidad entre compromisos originales, reprogramaciones y registros de avance, sin contabilizar dos veces los resultados.

## Ejemplo aprobado por el PO

Hoy se planifica estudiar Rails durante 60 minutos y se registran 35 minutos realizados. Para continuar mañana y cerrar hoy, se justifica la reprogramación con categoría y explicación textual, y se indica mañana como destino.

El compromiso de hoy queda resuelto como **REPROGRAMADO**, conservando planificación original de 60 minutos y ejecución de 35 minutos. Se crea un compromiso de continuación para mañana, vinculado a la misma tarea, pendiente de 25 minutos. La tarea conserva progreso acumulado de 35/60 minutos; mañana se visualizan tanto el compromiso pendiente de 25 minutos como el acumulado.

Los 35 minutos cuentan únicamente como esfuerzo realizado hoy. La reprogramación no cuenta como cumplimiento del compromiso original. Alcanzar 60 minutos acumulados no completa automáticamente la tarea: requiere confirmación explícita.

Los valores 60/35/25 y 35/60 pertenecen al caso aprobado. No se aprueba aquí una fórmula general para otras métricas, sobrecumplimiento, cambios de meta o estadísticas.

## Precisiones posteriores — CONFIRMADAS por el PO

### Metas cuantitativas opcionales

El caso 60 minutos planificados, 35 realizados y 25 restantes tiene una meta cuantitativa definida. No todas las tareas tendrán métricas cuantitativas; no se presupone cálculo automático del trabajo restante. Para una tarea sin meta medible, la reprogramación permite continuar el trabajo sin exigir una cantidad restante numérica.

Esta aprobación resuelve el carácter opcional de las metas cuantitativas, previamente propuesto dentro de DEC-37/RF-006. No aprueba los demás atributos o funciones agrupados en esa propuesta ni una fórmula general.

### Finalización de tarea y resolución de compromiso

La tarea y sus compromisos diarios mantienen estados independientes. En el ejemplo cuantitativo, tras registrar mañana los 25 minutos restantes y confirmar explícitamente la finalización, la tarea puede marcarse completada y el compromiso de mañana queda resuelto como completado. El compromiso original permanece REPROGRAMADO; los avances mantienen sus fechas reales y la finalización no modifica retroactivamente el resultado del compromiso original.

No generalizar este vínculo de finalización/resolución a hábitos recurrentes ni a tareas sin metas cuantitativas. Las correcciones históricas justificadas y auditadas siguen reguladas por RN-20/RN-28: la finalización del ejemplo no constituye una corrección histórica.

## Criterios de aceptación — CONFIRMADOS

Los identificadores se conservan tras la aprobación. La versión vigente de los criterios está en el borrador del PRD; la tabla siguiente preserva el texto aprobado antes de las dos precisiones posteriores. La frase de CA-DEC62-08 que mantenía abierta la relación tarea/compromiso se sustituye para el ejemplo cuantitativo por la precisión aprobada, sin generalizar a otros casos.

| ID | Escenario y resultado esperado | Trazabilidad de descubrimiento |
|---|---|---|
| CA-DEC62-01 | Dada una tarea comprometida para hoy, al reprogramarla a mañana, ambos compromisos se vinculan a la misma tarea. Reprogramaciones sucesivas conservan esa identidad; no se especifica aquí cómo resolver coincidencias. | RF-027; RN-11; DEC-11 y nueva aprobación DEC-62; límite DEC-67. |
| CA-DEC62-02 | Con el caso 60 minutos planificados y 35 realizados, una reprogramación válida deja el compromiso de hoy REPROGRAMADO, preservando sus 60 planificados y 35 ejecutados. | RF-012, RF-017, RF-027; RN-07, RN-11, RN-18; DEC-07, DEC-11, DEC-18 y DEC-62. |
| CA-DEC62-03 | Ante ausencia de categoría, explicación textual o fecha de destino, no se permite resolver el compromiso por reprogramación. Mientras ese compromiso siga sin resolver, no se permite cerrar la jornada. Validación exacta del texto queda pendiente. | RF-025, RF-026, RF-027; RN-03, RN-05, RN-06; DEC-03, DEC-05, DEC-06; pendiente DEC-65. |
| CA-DEC62-04 | Tras la reprogramación válida del ejemplo, mañana tiene un compromiso propio pendiente de 25 minutos y su planificación, estado y resolución son independientes de los del compromiso de hoy. | RF-027; RN-06, RN-11; DEC-06, DEC-11 y DEC-62. |
| CA-DEC62-05 | Al consultar mañana el caso, se visualizan el compromiso pendiente de 25 minutos y el progreso acumulado de la misma tarea de 35/60 minutos. No se prescribe pantalla, navegación ni componente. | RF-017, RF-019; RN-07, RN-17; DEC-07, DEC-17 y DEC-62. |
| CA-DEC62-06 | Los 35 minutos registrados hoy permanecen atribuidos a hoy. Crear el compromiso de mañana no produce un segundo registro de esos 35 minutos ni los atribuye al esfuerzo de mañana. | RF-017, RF-019; RN-16, RN-26; DEC-16, DEC-26 y DEC-62. |
| CA-DEC62-07 | El compromiso de hoy se conserva en historial y en el conjunto que cuenta para cumplimiento; su resolución REPROGRAMADO no se contabiliza como completado. No se establece un porcentaje final de cumplimiento. | RF-027, RF-035; RN-11, RN-25; DEC-11, DEC-25; fórmulas pendientes DEC-63. |
| CA-DEC62-08 | Si mañana se registran los 25 minutos restantes, la tarea muestra 60/60 minutos acumulados, sin completarse automáticamente. Su completado requiere confirmación explícita. La relación exacta entre completar tarea y resolver compromiso permanece abierta. | RF-018, RF-019; RN-15, RN-17, RN-26; DEC-15, DEC-17, DEC-26 y DEC-62. |
| CA-DEC62-09 | En el caso aprobado, puede reconstruirse la relación entre tarea, compromiso original de hoy, reprogramación a mañana, compromiso de continuación y avance de hoy. El avance previo conserva una sola contribución al acumulado. No se prescribe un mecanismo de almacenamiento o consulta. | RF-012, RF-017, RF-019, RF-027; RNF-002; RN-11, RN-18, RN-26; DEC-11, DEC-18, DEC-26 y DEC-62. |

## Preguntas que permanecen abiertas

- **DEC-62:** definición exacta de ejecución frente a registro de avance; alcance de incorporación formal fuera del guardado confirmado en jornada abierta; retiro y su encaje con las tres resoluciones; jornada comprometida; catálogo completo de estados/transiciones y relación entre completado de tarea y resolución de compromiso fuera del ejemplo cuantitativo aprobado.
- **DEC-67:** reprogramaciones sucesivas, fechas admisibles, coincidencias y recurrencias.
- **DEC-74 y DEC-63:** metas de cantidad/porcentaje, cambios de meta, sobrecumplimiento, contribución a objetivos, fórmulas y denominadores generales.
- **DEC-60, DEC-61 y DEC-68:** registro antes de apertura, actividades después del cierre y atribución después de medianoche.

No se aprueban esquema de base de datos, nombres de modelos Rails, tecnología de trazabilidad ni fórmulas adicionales. Tampoco se establece que el usuario deba abrir la jornada de mañana para recibir el compromiso de continuación.

## Incorporación en jornada abierta — decisión y criterios CONFIRMADOS

**Origen:** confirmación explícita del PO durante la elaboración del PRD. Guardar una tarea asignada a una jornada abierta crea automáticamente su compromiso diario, sin segunda acción de confirmación. Posteriormente el PO aprobó explícitamente CA-DEC62-10 a CA-DEC62-16 y confirmó CA-DEC62-17, añadiendo que el sistema informa cuando la incorporación no se completa correctamente.

**Alcance de esta revisión:** creación y guardado de una tarea nueva asignada a una jornada abierta. Los criterios no definen asignaciones a fechas futuras, comportamiento de tareas recurrentes, guardados repetidos, compromisos duplicados ni asignación de una tarea existente. Se conserva la decisión explícita tal como la entregó el PO; esos casos adicionales no se desarrollan por inferencia.

### Ambigüedades detectadas

- Guardar se refiere al resultado exitoso de guardar tarea y asignación; la conducta ante fallos se confirmó posteriormente en CA-DEC62-17, incluida la información al usuario.
- Fecha significa la fecha de la jornada seleccionada, no necesariamente la fecha del momento de guardar. No decide asignaciones futuras ni modifica la fecha real de avances.
- La planificación original de una tarea incorporada durante el día es la asumida al incorporarla, no una planificación reconstruida como si existiera al abrir la jornada.
- Registrar avance en CA-DEC62-16 se limita a una tarea con compromiso ya incorporado a esa jornada. No decide qué ocurre al registrar trabajo sin compromiso, antes de abrir o después de cerrar.
- CA-DEC62-10 y CA-DEC62-12 se solapan: el primero comprueba creación automática y el segundo ausencia de confirmación adicional. Se conservan los IDs solicitados.
- CA-DEC62-17 confirma integridad observable de la incorporación conjunta, sin seleccionar transacciones, modelos o mecanismo de recuperación. Solo contempla la tarea nueva de esta operación; no prescribe eliminar tareas preexistentes.

### Versión vigente aprobada — todos CONFIRMADOS

| ID | Criterio revisado | Estado | Trazabilidad |
|---|---|---|---|
| CA-DEC62-10 | Dada una jornada abierta, al guardar correctamente una tarea nueva asignada a ella, se crea automáticamente su compromiso diario. | CONFIRMADO | RF-010, RF-011; RN-02; DEC-36 y nueva confirmación DEC-62. |
| CA-DEC62-11 | El compromiso creado queda vinculado a la tarea guardada y a la jornada seleccionada, con la fecha de esa jornada. | CONFIRMADO | RF-010, RF-011; DEC-62. El vínculo conceptual procede de DEC-62, no de una RN adicional inventada. |
| CA-DEC62-12 | La incorporación ocurre al guardar, sin requerir una segunda acción para aceptar o confirmar el compromiso. | CONFIRMADO | RF-011, RF-035; RN-25; DEC-25 y DEC-62. |
| CA-DEC62-13 | Después del guardado correcto, al consultar la planificación de esa jornada se encuentra el compromiso incorporado. No se fija pantalla, mecanismo de actualización ni umbral de latencia. | CONFIRMADO | RF-011; RN-02; DEC-50 y DEC-62. |
| CA-DEC62-14 | El compromiso incorporado debe resolverse mediante cumplimiento, cancelación o reprogramación; mientras siga sin resolver, bloquea el cierre. Cancelar/reprogramar exige categoría y texto; reprogramar exige fecha destino. | CONFIRMADO | RF-025, RF-026, RF-027; RN-03, RN-04, RN-05, RN-06; DEC-03 a DEC-06 y DEC-62. |
| CA-DEC62-15 | El compromiso incorporado durante la jornada se incluye en el conjunto de compromisos asumidos para cumplimiento. Conserva la planificación original asumida al incorporarlo y registra cambios posteriores; no se define una fórmula o porcentaje. | CONFIRMADO | RF-012, RF-035; RN-18, RN-25; DEC-18, DEC-25 y DEC-62; fórmulas pendientes DEC-63. |
| CA-DEC62-16 | Dada una tarea con compromiso ya incorporado a esa jornada, registrar un avance asociado no crea por sí mismo otro compromiso. La fecha del trabajo sigue siendo su fecha real de ejecución. | CONFIRMADO | RF-017, RF-019; RN-16, RN-26; DEC-16, DEC-26 y DEC-62. La ausencia de creación fue confirmada explícitamente por el PO; no se deduce automáticamente de RN-26. |
| CA-DEC62-17 | En el guardado conjunto de una tarea nueva y su compromiso, si falla la creación de cualquiera, la operación no deja incorporada solo la tarea nueva o solo el compromiso: no permanece una incorporación parcial. El sistema informa que la incorporación no se completó correctamente. No se prescribe mecanismo técnico. | CONFIRMADO | DEC-62, aprobación explícita de CA-DEC62-17; relación con RNF-003, RN-12 y DEC-12: se confirma esta garantía observable para incorporación, sin aprobar mecanismos técnicos ni el alcance completo de esas propuestas. |

Los ocho criterios se incorporan al borrador con sus identificadores y trazabilidad. CA-DEC62-17 cambió de PROPUESTO a CONFIRMADO por aprobación explícita del PO; su alcance incluye información de fallo y ausencia de incorporación parcial, sin seleccionar implementación. No se promueven en bloque RN-12, RNF-003 ni DEC-12.

**Pendientes expresamente conservados:** asignaciones a fechas futuras; posibles compromisos duplicados; recurrencias; registro de avances sin compromiso previo; conceptos restantes de DEC-62. La definición de tarea activa y la distinción de cancelación se confirmaron posteriormente en el bloque siguiente; el mecanismo para resolver compromisos abiertos se confirmó posteriormente, con preparación sin efectos y confirmación final consistente.

## Tarea activa y cancelación definitiva — CONFIRMADO

**Origen:** confirmación explícita del PO en la conversación PRD. El mensaje duplicó el mismo contenido; se registra una sola decisión, sin duplicar criterios.

- Una tarea permanece activa mientras exista intención de continuarla o realizarla, aunque no tenga compromisos diarios programados. Cancelar o reprogramar un compromiso de una fecha no modifica automáticamente el estado de la tarea general. La tarea continúa disponible para incorporarse a futuras jornadas; el mecanismo de asignación futura sigue pendiente.
- Cancelar definitivamente una tarea es una acción explícita distinta de cancelar un compromiso diario. Requiere justificación y conserva identidad, descripción, avances previos, compromisos históricos, reprogramaciones anteriores y fecha/motivo de cancelación definitiva.
- La cancelación definitiva no borra ni modifica retroactivamente resultados históricos. Esta acción no equivale a una corrección histórica de RN-20/RN-28.
- No se permite que la cancelación definitiva deje compromisos diarios abiertos sin resolver. El mecanismo funcional se confirmó posteriormente: revisión individual, decisiones preparadas y confirmación final consistente, sin cancelación silenciosa ni propagación automática; véase el bloque vigente siguiente.
- No generalizar estas reglas a hábitos recurrentes. No se especifican modelos, tablas, endpoints ni componentes.

### CA-DEC62-18 a CA-DEC62-25 — CONFIRMADOS e incorporados al borrador

| ID | Criterio verificable | Estado | Origen / trazabilidad |
|---|---|---|---|
| CA-DEC62-18 | Mientras exista intención de continuar o realizar una tarea, la ausencia de compromisos diarios programados no la vuelve inactiva. | CONFIRMADO | DEC-62, nueva confirmación PO. RN-29/RF-007 usan tarea activa; esta definición aclara su significado sin cambiar el archivo de objetivos. |
| CA-DEC62-19 | Cancelar o reprogramar un compromiso diario no modifica automáticamente el estado de la tarea general. | CONFIRMADO | DEC-62; RF-025/RF-027; RN-04/RN-11. La independencia proviene de la nueva confirmación PO. |
| CA-DEC62-20 | Una tarea que sigue activa tras cancelar o reprogramar su compromiso continúa disponible para incorporación a otras jornadas. No fija reglas de asignación futura, duplicados o recurrencias. | CONFIRMADO | DEC-62; RF-010/RF-011. |
| CA-DEC62-21 | La cancelación definitiva de una tarea requiere una acción explícita distinta de cancelar un compromiso diario; cancelar solo el compromiso no ejecuta esa acción. | CONFIRMADO | DEC-62; distinción con RF-025/RN-04. |
| CA-DEC62-22 | Sin justificación no se permite confirmar la cancelación definitiva de la tarea. No se exige por inferencia una categoría adicional ni se define validación textual concreta. | CONFIRMADO | DEC-62, nueva confirmación PO. RN-05/DEC-05 se aplican a compromisos y no definen el formato de esta justificación. |
| CA-DEC62-23 | Después de cancelar definitivamente, se conservan identidad y descripción de tarea, avances previos, compromisos históricos y reprogramaciones anteriores; se registran fecha y motivo de cancelación definitiva. | CONFIRMADO | DEC-62; RNF-002 como antecedente de conservación, sin afirmar que ese requisito ya definía cancelación definitiva. |
| CA-DEC62-24 | La cancelación definitiva por sí misma no borra ni cambia resultados históricos ni fechas de los avances registrados. | CONFIRMADO | DEC-62; RF-017/RNF-002; RN-16; RN-20/RN-28 no se usan para justificar cambios automáticos. |
| CA-DEC62-25 | No se confirma una cancelación definitiva cuyo resultado deje compromisos diarios abiertos sin resolver. El mecanismo funcional fue aprobado posteriormente: preparación individual y aplicación consistente en confirmación final. | CONFIRMADO | DEC-62, nueva invariante PO; relación con RF-025/RN-03/RN-04. |

### Mecanismo vigente — CONFIRMADO por el PO

Al solicitar cancelación definitiva, el sistema muestra compromisos asociados sin resolver. El usuario prepara individualmente cumplimiento cuando corresponda o cancelación con categoría y explicación obligatorias. No se permite confirmar mientras exista un compromiso sin resolución preparada válida. Preparar decisiones no modifica inmediatamente los compromisos: solo la confirmación final explícita aplica conjuntamente las resoluciones y la cancelación definitiva de forma consistente.

Si se decide continuar mediante reprogramación, se debe desistir de la cancelación definitiva y mantener la tarea activa. No se prescribe aquí el flujo posterior de reprogramación ni se aplica una resolución al abandonar este formulario.

Al abandonar sin confirmar, la tarea permanece activa y no se aplican resoluciones parciales. Si falla la operación final, no queda una cancelación parcialmente aplicada. Se aprueba comportamiento observable, no transacciones u otro mecanismo técnico. No se aprueba propagación silenciosa o automática.

**Conciliación con la condición de bloqueo:** las resoluciones preparadas deben cubrir todos los compromisos sin resolver antes de permitir la confirmación final; su aplicación ocurre junto con la cancelación definitiva. Esto preserva la prohibición de dejar compromisos abiertos sin resolver, sin exigir que los cambios se apliquen antes de confirmar.

### CA-DEC62-26 a CA-DEC62-33 — CONFIRMADOS e incorporados al borrador

| ID | Criterio verificable | Estado | Trazabilidad |
|---|---|---|---|
| CA-DEC62-26 | Al solicitar cancelación definitiva, se muestran los compromisos asociados que aún no están resueltos. | CONFIRMADO | DEC-62, mecanismo aprobado; RF-025/RN-04 como antecedentes de resolución. |
| CA-DEC62-27 | El usuario prepara una resolución individual para cada compromiso: cumplimiento cuando corresponda o cancelación con categoría y explicación obligatorias. No se aplica una resolución común silenciosamente. | CONFIRMADO | DEC-62; RF-025/RF-026; RN-04/RN-05. |
| CA-DEC62-28 | Si algún compromiso sin resolver carece de una resolución preparada válida, no se permite confirmar la cancelación definitiva. Una cancelación preparada sin categoría o explicación no satisface esta condición. | CONFIRMADO | DEC-62; CA-DEC62-22/25; RF-026; RN-05. |
| CA-DEC62-29 | Preparar o cambiar decisiones dentro del formulario no modifica los estados ni resultados efectivos de los compromisos y no cancela definitivamente la tarea. | CONFIRMADO | DEC-62, aprobación explícita de preparación sin efectos. |
| CA-DEC62-30 | Si el usuario abandona sin confirmación final, la tarea permanece activa y no se aplica ninguna de las resoluciones preparadas, aunque estuvieran preparadas todas. | CONFIRMADO | DEC-62, comportamiento aprobado de abandono. |
| CA-DEC62-31 | Con justificación de la tarea y resoluciones válidas preparadas para todos sus compromisos sin resolver, la confirmación final explícita aplica esas resoluciones y la cancelación definitiva conjuntamente; al completarse, no queda un compromiso abierto sin resolver. Se conserva el historial exigido por CA-DEC62-23/24. | CONFIRMADO | DEC-62; CA-DEC62-21 a CA-DEC62-25; RNF-002 como antecedente. |
| CA-DEC62-32 | Si falla la aplicación final, no queda aplicada solo la cancelación definitiva o solo parte de sus resoluciones: los cambios de esa operación no quedan parcialmente aplicados. No se prescribe mecanismo técnico. | CONFIRMADO | DEC-62, garantía explícita aprobada; RNF-003/RN-12 como antecedentes propuestos, sin promoverlos en bloque. |
| CA-DEC62-33 | Si el usuario decide continuar mediante reprogramación, desiste de la cancelación definitiva y la tarea permanece activa; las resoluciones preparadas en ese formulario no se aplican por ese desistimiento. El flujo de reprogramación posterior no se define aquí. | CONFIRMADO | DEC-62; CA-DEC62-19; RF-027/RN-06 como antecedentes de reprogramación. |

### Pendientes conservados

Reglas específicas de hábitos recurrentes; asignaciones futuras; duplicados; avances sin compromiso previo; ejecución frente a registro de avance; retiro y jornada comprometida; formato exacto de justificación definitiva; posible reactivación; tratamiento de cambios concurrentes durante preparación/confirmación y recuperación o comunicación ante fallos. No se infieren soluciones técnicas ni comportamientos adicionales.

## Catálogos efectivos e inicializaciones — CONFIRMADOS para el MVP

Aprobación explícita del PO: catálogo exhaustivo de tarea general **ACTIVA, COMPLETADA, CANCELADA_DEFINITIVAMENTE**; catálogo exhaustivo de compromiso diario **PENDIENTE, COMPLETADO, CANCELADO, REPROGRAMADO**. Toda tarea nueva comienza ACTIVA y todo compromiso diario nuevo PENDIENTE. Los estados son independientes. No existe estado efectivo EN_PROGRESO por avances parciales ni EN_CANCELACIÓN por preparación del formulario.

La aprobación del catálogo no aprueba todas las transiciones. Se conservan las confirmadas: cumplimiento explícito y coordinación con compromiso en el ejemplo cuantitativo (CA-08/RN-15); resolución diaria por cumplimiento, cancelación y reprogramación con sus condiciones (RN-04 a RN-06); cancelación definitiva consistente con resoluciones preparadas aplicadas en confirmación final (CA-21 a CA-33); ausencia de cambios efectivos por preparación o abandono; cancelar/reprogramar compromiso no modifica automáticamente la tarea (CA-19).

**PENDIENTES explícitos:** reactivación de tareas completadas/canceladas; correcciones de resoluciones históricas (el principio de corrección auditada RN-20/RN-28 permanece confirmado, no sus transiciones concretas); finalización de tareas sin metas cuantitativas; comportamiento particular de recurrencias; asignaciones futuras y prevención de duplicados; estados y transiciones de jornadas. Apertura/cierre manuales y sus invariantes previamente confirmadas se conservan: no se infiere de ellas un catálogo de jornadas.

### CA-DEC62-34 a CA-DEC62-41 — CONFIRMADOS e incorporados al borrador

| ID | Criterio verificable | Estado | Trazabilidad |
|---|---|---|---|
| CA-DEC62-34 | El estado efectivo de toda tarea general del MVP pertenece exclusivamente a ACTIVA, COMPLETADA o CANCELADA_DEFINITIVAMENTE. | CONFIRMADO | DEC-62, aprobación explícita del catálogo; CA-18/21 como antecedentes. |
| CA-DEC62-35 | El estado efectivo de todo compromiso diario del MVP pertenece exclusivamente a PENDIENTE, COMPLETADO, CANCELADO o REPROGRAMADO. | CONFIRMADO | DEC-62; RN-04 y CA-02 como antecedentes de resoluciones. |
| CA-DEC62-36 | Al crear correctamente una tarea nueva, su estado efectivo inicial es ACTIVA. No decide asignación a jornadas futuras. | CONFIRMADO | DEC-62, inicialización explícita; RF-010. |
| CA-DEC62-37 | Al crear correctamente un compromiso diario nuevo, su estado efectivo inicial es PENDIENTE. Aplica al origen y la continuación de los casos ya aprobados, sin definir generación futura/recurrencias ni duplicados. | CONFIRMADO | DEC-62, inicialización explícita; CA-04/10/11; RF-027/RF-011. |
| CA-DEC62-38 | Los estados de tarea y compromiso se mantienen separados: cancelar/reprogramar un compromiso de una tarea ACTIVA no cambia por sí mismo esa tarea. En el ejemplo cuantitativo aprobado, al completar la continuación, tarea y compromiso de destino se completan y el original permanece REPROGRAMADO. | CONFIRMADO | DEC-62; CA-08/19; RN-11/RN-15. |
| CA-DEC62-39 | Registrar avances parciales no crea un estado efectivo EN_PROGRESO en la tarea o el compromiso; cualquier estado efectivo pertenece a su catálogo y se conservan las condiciones de confirmación explícita previamente aprobadas. | CONFIRMADO | DEC-62; CA-08/16; RN-15. No fija aquí otras transiciones por registrar avances. |
| CA-DEC62-40 | Preparar una cancelación definitiva no crea estado efectivo EN_CANCELACIÓN ni altera estados efectivos de tarea/compromisos. Abandonar conserva esos estados; la confirmación válida aplica las transiciones aprobadas conjuntamente. | CONFIRMADO | DEC-62; CA-29/30/31/32. |
| CA-DEC62-41 | Definir los catálogos no habilita automáticamente todas las combinaciones de transición. Reactivaciones y correcciones de resoluciones históricas siguen sin una transición aprobada; solo se especifican aquí las transiciones previamente confirmadas. | CONFIRMADO | DEC-62; pendientes DEC-69; RN-20/RN-28 conservan sus principios confirmados. Este criterio controla el alcance del PRD, no prescribe un comportamiento de rechazo o interfaz. |

No se agregan estados o reglas para hábitos, jornadas o asignaciones futuras. Los ocho criterios fueron aprobados por el PO; el PRD permanece draft. CA-DEC62-41 es una restricción de alcance de la especificación, sin prescribir rechazo de transiciones indefinidas. DEC-62 sigue parcialmente abierta; no se añaden más criterios en esta iteración.
