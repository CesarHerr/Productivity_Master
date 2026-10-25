---
title: PRD — Productivity_Master
status: draft
created: 2026-10-11
updated: 2026-10-12
---

# PRD — Productivity_Master

## Propósito y estado

Borrador inicial del flujo interactivo `bmad-prd`. El Product Owner aprobó iniciar la fase PRD y crear/activar esta iniciativa. No constituye un PRD terminado ni autorización de implementación.

Las decisiones CONFIRMADAS del descubrimiento son requisitos aprobados. Las PROPUESTAS conservan ese estado. DEC-62 tiene una resolución parcial aprobada durante la fase PRD; sus aspectos restantes y las demás preguntas DEC-60 a DEC-75 siguen PENDIENTES. No se consolidarán definiciones ni comportamientos nuevos sin aprobación explícita del Product Owner.

## Fuentes aprobadas

- [Product Brief](../../../docs/discovery/product-brief.md).
- [Línea base de requisitos](../../../docs/discovery/requirements-baseline.md).
- [Reglas de negocio](../../../docs/discovery/business-rules.md).
- [Registro de decisiones](../../../docs/discovery/decision-log.md).

La elaboración conservará los identificadores RF, RN y DEC de origen, mediante referencias junto a los requisitos y criterios verificables del PRD.

## Glosario — definiciones aprobadas parcialmente

- **Tarea activa:** existe intención de continuarla o realizarla, aunque no tenga compromisos diarios programados. Cancelar o reprogramar un compromiso no modifica automáticamente el estado de la tarea. Origen: DEC-62, aprobación explícita del PO. Los criterios de este nuevo bloque esperan revisión.
- **Tarea:** mantiene su identidad a través de los días y reprogramaciones. Sus estados son independientes de los estados de sus compromisos diarios. Puede carecer de meta cuantitativa. Origen: DEC-62, aprobación explícita durante PRD.
- **Compromiso diario:** corresponde a una fecha en que se asume realizar una tarea, con planificación, estado y resolución propios. Origen: DEC-62.
- **Registro de avance:** representa trabajo realmente realizado y se atribuye a su fecha de ejecución. Origen: DEC-62; RF-017; RN-16; DEC-16.
- **Ejecución:** definición exacta frente al registro de avance PENDIENTE; no se establece un concepto adicional por inferencia.

## Funcionalidad — continuidad de tareas y compromisos diarios

**Estado:** CONFIRMADO, con alcance parcial de DEC-62. Los criterios siguientes fueron aprobados explícitamente por el PO. El PRD continúa en borrador; las definiciones restantes no están aprobadas. Historial de aprobación y precisiones: [DEC-62](decision-dec-62.md).

### FR-1 — Continuidad, reprogramación y progreso

El usuario puede continuar una tarea en otra fecha conservando su identidad, el compromiso original, los avances parciales y la trazabilidad. Cada fecha asumida tiene un compromiso diario con planificación, estado y resolución independientes. Los avances pertenecen a su fecha real y no se contabilizan dos veces.

**Metas opcionales:** el ejemplo 60/35/25 tiene una meta definida. Una tarea sin meta medible puede reprogramarse para continuar sin exigir cantidad restante numérica. No se presupone un cálculo automático del trabajo restante para todas las tareas.

**Origen:** RF-012, RF-017, RF-019, RF-027; RNF-002; RN-07, RN-11, RN-16, RN-18, RN-26; DEC-62 y precisiones del PO. La ausencia de métricas, antes propuesta en RF-006/DEC-37, se confirma exclusivamente para este aspecto; las demás propuestas de esos registros no se aprueban por asociación.

**Criterios de aceptación CONFIRMADOS:**

#### CA-DEC62-01

Dada una tarea comprometida para hoy, al reprogramarla a mañana, ambos compromisos se vinculan a la misma tarea. Reprogramaciones sucesivas conservan esa identidad; no se especifica aquí cómo resolver coincidencias.

**Origen:** RF-027; RN-11; DEC-11 y nueva aprobación DEC-62; límite DEC-67.

#### CA-DEC62-02

Con el caso 60 minutos planificados y 35 realizados, una reprogramación válida deja el compromiso de hoy REPROGRAMADO, preservando sus 60 planificados y 35 ejecutados.

**Origen:** RF-012, RF-017, RF-027; RN-07, RN-11, RN-18; DEC-07, DEC-11, DEC-18 y DEC-62.

#### CA-DEC62-03

Ante ausencia de categoría, explicación textual o fecha de destino, no se permite resolver el compromiso por reprogramación. Mientras ese compromiso siga sin resolver, no se permite cerrar la jornada. Validación exacta del texto queda pendiente.

**Origen:** RF-025, RF-026, RF-027; RN-03, RN-05, RN-06; DEC-03, DEC-05, DEC-06; pendiente DEC-65.

#### CA-DEC62-04

Tras la reprogramación válida del ejemplo, mañana tiene un compromiso propio pendiente de 25 minutos y su planificación, estado y resolución son independientes de los del compromiso de hoy.

**Origen:** RF-027; RN-06, RN-11; DEC-06, DEC-11 y DEC-62.

#### CA-DEC62-05

Al consultar mañana el caso, se visualizan el compromiso pendiente de 25 minutos y el progreso acumulado de la misma tarea de 35/60 minutos. No se prescribe pantalla, navegación ni componente.

**Origen:** RF-017, RF-019; RN-07, RN-17; DEC-07, DEC-17 y DEC-62.

#### CA-DEC62-06

Los 35 minutos registrados hoy permanecen atribuidos a hoy. Crear el compromiso de mañana no produce un segundo registro de esos 35 minutos ni los atribuye al esfuerzo de mañana.

**Origen:** RF-017, RF-019; RN-16, RN-26; DEC-16, DEC-26 y DEC-62.

#### CA-DEC62-07

El compromiso de hoy se conserva en historial y en el conjunto que cuenta para cumplimiento; su resolución REPROGRAMADO no se contabiliza como completado. No se establece un porcentaje final de cumplimiento.

**Origen:** RF-027, RF-035; RN-11, RN-25; DEC-11, DEC-25; fórmulas pendientes DEC-63.

#### CA-DEC62-08

Si mañana se registran los 25 minutos restantes, la tarea muestra 60/60 acumulados sin completarse automáticamente. Cuando el usuario confirma explícitamente la finalización, la tarea puede marcarse completada y el compromiso de mañana queda resuelto como completado. El compromiso original permanece REPROGRAMADO; los avances mantienen sus fechas reales y no se modifica retroactivamente su resultado. Este comportamiento se limita al ejemplo cuantitativo aprobado; no se extiende a hábitos recurrentes ni a tareas sin metas cuantitativas.

**Origen:** RF-018, RF-019; RN-15, RN-17, RN-26; DEC-15, DEC-17, DEC-26 y DEC-62.

#### CA-DEC62-09

En el caso aprobado, puede reconstruirse la relación entre tarea, compromiso original de hoy, reprogramación a mañana, compromiso de continuación y avance de hoy. El avance previo conserva una sola contribución al acumulado. No se prescribe un mecanismo de almacenamiento o consulta.

**Origen:** RF-012, RF-017, RF-019, RF-027; RNF-002; RN-11, RN-18, RN-26; DEC-11, DEC-18, DEC-26 y DEC-62.

### FR-2 — Continuación sin meta cuantitativa

El usuario puede reprogramar una tarea sin meta medible para continuar el trabajo en otra fecha, sin que la aplicación exija una cantidad restante numérica. Se mantienen las condiciones confirmadas de reprogramación: categoría, explicación y fecha destino.

**Origen:** RF-006 (solo opcionalidad de métricas, confirmada durante PRD), RF-026, RF-027; RN-05, RN-06; DEC-37 (solo ese aspecto), DEC-62 y precisión explícita del PO. Este requisito documenta la aprobación funcional; no agrega un criterio CA nuevo a los nueve aprobados.

### FR-3 — Incorporación automática en jornada abierta

**Estado:** CONFIRMADO. Guardar una tarea nueva asignada a una jornada abierta crea automáticamente su compromiso diario, sin segunda acción de confirmación. Queda sujeto a resolución, cierre, historial y contabilización de compromisos asumidos. La incorporación conjunta es consistente: si falla la creación de la tarea nueva o de su compromiso, no queda solo uno incorporado y el sistema informa que la incorporación no se completó correctamente.

**Origen:** RF-010, RF-011, RF-012, RF-017, RF-019, RF-025, RF-026, RF-027, RF-035; RN-02, RN-03 a RN-06, RN-16, RN-18, RN-25, RN-26; DEC-62 y aprobación explícita de CA-DEC62-10 a CA-DEC62-17. RNF-003/RN-12/DEC-12 se relacionan con la garantía de integridad, pero sus mecanismos y alcance restantes continúan propuestos.

**Criterios de aceptación CONFIRMADOS:**

#### CA-DEC62-10

Dada una jornada abierta, al guardar correctamente una tarea nueva asignada a ella, se crea automáticamente su compromiso diario.

**Estado:** CONFIRMADO. **Origen:** RF-010, RF-011; RN-02; DEC-36 y nueva confirmación DEC-62.

#### CA-DEC62-11

El compromiso creado queda vinculado a la tarea guardada y a la jornada seleccionada, con la fecha de esa jornada.

**Estado:** CONFIRMADO. **Origen:** RF-010, RF-011; DEC-62. El vínculo conceptual procede de DEC-62, no de una RN adicional inventada.

#### CA-DEC62-12

La incorporación ocurre al guardar, sin requerir una segunda acción para aceptar o confirmar el compromiso.

**Estado:** CONFIRMADO. **Origen:** RF-011, RF-035; RN-25; DEC-25 y DEC-62.

#### CA-DEC62-13

Después del guardado correcto, al consultar la planificación de esa jornada se encuentra el compromiso incorporado. No se fija pantalla, mecanismo de actualización ni umbral de latencia.

**Estado:** CONFIRMADO. **Origen:** RF-011; RN-02; DEC-50 y DEC-62.

#### CA-DEC62-14

El compromiso incorporado debe resolverse mediante cumplimiento, cancelación o reprogramación; mientras siga sin resolver, bloquea el cierre. Cancelar/reprogramar exige categoría y texto; reprogramar exige fecha destino.

**Estado:** CONFIRMADO. **Origen:** RF-025, RF-026, RF-027; RN-03, RN-04, RN-05, RN-06; DEC-03 a DEC-06 y DEC-62.

#### CA-DEC62-15

El compromiso incorporado durante la jornada se incluye en el conjunto de compromisos asumidos para cumplimiento. Conserva la planificación original asumida al incorporarlo y registra cambios posteriores; no se define una fórmula o porcentaje.

**Estado:** CONFIRMADO. **Origen:** RF-012, RF-035; RN-18, RN-25; DEC-18, DEC-25 y DEC-62; fórmulas pendientes DEC-63.

#### CA-DEC62-16

Dada una tarea con compromiso ya incorporado a esa jornada, registrar un avance asociado no crea por sí mismo otro compromiso. La fecha del trabajo sigue siendo su fecha real de ejecución.

**Estado:** CONFIRMADO. **Origen:** RF-017, RF-019; RN-16, RN-26; DEC-16, DEC-26 y DEC-62. La ausencia de creación fue confirmada explícitamente por el PO; no se deduce automáticamente de RN-26.

#### CA-DEC62-17

En el guardado conjunto de una tarea nueva y su compromiso, si falla la creación de cualquiera, la operación no deja incorporada solo la tarea nueva o solo el compromiso: no permanece una incorporación parcial. El sistema informa que la incorporación no se completó correctamente. No se prescribe mecanismo técnico.

**Estado:** CONFIRMADO. **Origen:** DEC-62, aprobación explícita de CA-DEC62-17; relación con RNF-003, RN-12 y DEC-12: se confirma esta garantía observable para incorporación, sin aprobar mecanismos técnicos ni el alcance completo de esas propuestas.

### FR-4 — Tarea activa y cancelación definitiva

**Estado:** CONFIRMADO. Una tarea sigue activa mientras exista intención de realizarla o continuarla, aunque no tenga compromisos programados. Cancelar o reprogramar un compromiso diario no cambia automáticamente la tarea. La cancelación definitiva es explícita y justificada, distinta de resolver un compromiso; conserva identidad, descripción, avances, compromisos, reprogramaciones y fecha/motivo sin alterar retroactivamente resultados. No puede dejar compromisos diarios sin resolver.

**Origen:** DEC-62, confirmaciones explícitas del PO. Antecedentes: RF-007/RN-29 para significado de activa; RF-025/RN-04 para resolución de compromisos; RF-017/RN-16 y RNF-002 para conservación. No se generaliza a hábitos recurrentes ni decide asignaciones futuras.

**Criterios CONFIRMADOS:**

#### CA-DEC62-18

Mientras exista intención de continuar o realizar una tarea, la ausencia de compromisos diarios programados no la vuelve inactiva.

**Estado:** CONFIRMADO. **Origen:** DEC-62, nueva confirmación PO. RN-29/RF-007 usan tarea activa; esta definición aclara su significado sin cambiar el archivo de objetivos.

#### CA-DEC62-19

Cancelar o reprogramar un compromiso diario no modifica automáticamente el estado de la tarea general.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RF-025/RF-027; RN-04/RN-11. La independencia proviene de la nueva confirmación PO.

#### CA-DEC62-20

Una tarea que sigue activa tras cancelar o reprogramar su compromiso continúa disponible para incorporación a otras jornadas. No fija reglas de asignación futura, duplicados o recurrencias.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RF-010/RF-011.

#### CA-DEC62-21

La cancelación definitiva de una tarea requiere una acción explícita distinta de cancelar un compromiso diario; cancelar solo el compromiso no ejecuta esa acción.

**Estado:** CONFIRMADO. **Origen:** DEC-62; distinción con RF-025/RN-04.

#### CA-DEC62-22

Sin justificación no se permite confirmar la cancelación definitiva de la tarea. No se exige por inferencia una categoría adicional ni se define validación textual concreta.

**Estado:** CONFIRMADO. **Origen:** DEC-62, nueva confirmación PO. RN-05/DEC-05 se aplican a compromisos y no definen el formato de esta justificación.

#### CA-DEC62-23

Después de cancelar definitivamente, se conservan identidad y descripción de tarea, avances previos, compromisos históricos y reprogramaciones anteriores; se registran fecha y motivo de cancelación definitiva.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RNF-002 como antecedente de conservación, sin afirmar que ese requisito ya definía cancelación definitiva.

#### CA-DEC62-24

La cancelación definitiva por sí misma no borra ni cambia resultados históricos ni fechas de los avances registrados.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RF-017/RNF-002; RN-16; RN-20/RN-28 no se usan para justificar cambios automáticos.

#### CA-DEC62-25

No se confirma una cancelación definitiva cuyo resultado deje compromisos diarios abiertos sin resolver. El mecanismo funcional fue aprobado posteriormente: preparación individual y aplicación consistente en confirmación final.

**Estado:** CONFIRMADO. **Origen:** DEC-62, nueva invariante PO; relación con RF-025/RN-03/RN-04.

### Mecanismo y criterios adicionales — CONFIRMADOS

Al solicitar cancelación definitiva se muestran compromisos asociados sin resolver. El usuario prepara individualmente cumplimiento o cancelación con categoría y explicación; preparar decisiones no cambia los compromisos. La confirmación final explícita requiere justificación de tarea y resoluciones válidas preparadas para todos los compromisos sin resolver, y aplica consistentemente las resoluciones y la cancelación definitiva. No se aplica una cancelación parcial ante fallo. Abandonar sin confirmar deja la tarea activa y no aplica resoluciones preparadas. Decidir continuar por reprogramación exige desistir de la cancelación definitiva y mantener la tarea activa.

**Origen:** aprobación explícita PO en DEC-62. CA-DEC62-26 a CA-DEC62-33 fueron aprobados explícitamente por el PO e incorporados a continuación; la aprobación está registrada en [la nota DEC-62](decision-dec-62.md). No se prescribe implementación.

#### CA-DEC62-26

Al solicitar cancelación definitiva, se muestran los compromisos asociados que aún no están resueltos.

**Estado:** CONFIRMADO. **Origen:** DEC-62, mecanismo aprobado; RF-025/RN-04 como antecedentes de resolución.

#### CA-DEC62-27

El usuario prepara una resolución individual para cada compromiso: cumplimiento cuando corresponda o cancelación con categoría y explicación obligatorias. No se aplica una resolución común silenciosamente.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RF-025/RF-026; RN-04/RN-05.

#### CA-DEC62-28

Si algún compromiso sin resolver carece de una resolución preparada válida, no se permite confirmar la cancelación definitiva. Una cancelación preparada sin categoría o explicación no satisface esta condición.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-DEC62-22/25; RF-026; RN-05.

#### CA-DEC62-29

Preparar o cambiar decisiones dentro del formulario no modifica los estados ni resultados efectivos de los compromisos y no cancela definitivamente la tarea.

**Estado:** CONFIRMADO. **Origen:** DEC-62, aprobación explícita de preparación sin efectos.

#### CA-DEC62-30

Si el usuario abandona sin confirmación final, la tarea permanece activa y no se aplica ninguna de las resoluciones preparadas, aunque estuvieran preparadas todas.

**Estado:** CONFIRMADO. **Origen:** DEC-62, comportamiento aprobado de abandono.

#### CA-DEC62-31

Con justificación de la tarea y resoluciones válidas preparadas para todos sus compromisos sin resolver, la confirmación final explícita aplica esas resoluciones y la cancelación definitiva conjuntamente; al completarse, no queda un compromiso abierto sin resolver. Se conserva el historial exigido por CA-DEC62-23/24.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-DEC62-21 a CA-DEC62-25; RNF-002 como antecedente.

#### CA-DEC62-32

Si falla la aplicación final, no queda aplicada solo la cancelación definitiva o solo parte de sus resoluciones: los cambios de esa operación no quedan parcialmente aplicados. No se prescribe mecanismo técnico.

**Estado:** CONFIRMADO. **Origen:** DEC-62, garantía explícita aprobada; RNF-003/RN-12 como antecedentes propuestos, sin promoverlos en bloque.

#### CA-DEC62-33

Si el usuario decide continuar mediante reprogramación, desiste de la cancelación definitiva y la tarea permanece activa; las resoluciones preparadas en ese formulario no se aplican por ese desistimiento. El flujo de reprogramación posterior no se define aquí.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-DEC62-19; RF-027/RN-06 como antecedentes de reprogramación.

## Catálogos efectivos e inicializaciones — CONFIRMADOS

Para el MVP, el catálogo exhaustivo de **tarea general** es ACTIVA, COMPLETADA, CANCELADA_DEFINITIVAMENTE. Toda tarea nueva comienza ACTIVA. El catálogo exhaustivo de **compromiso diario** es PENDIENTE, COMPLETADO, CANCELADO, REPROGRAMADO. Todo compromiso diario nuevo comienza PENDIENTE.

Los estados de tarea y compromiso son independientes. Avances parciales no crean estado efectivo EN_PROGRESO y preparar cancelación definitiva no crea EN_CANCELACIÓN. Aprobar estos catálogos no aprueba todas las transiciones posibles. Se conservan las transiciones y condiciones aprobadas en FR-1, FR-3 y FR-4, sin ampliar sus alcances.

**Origen:** aprobación explícita del PO en DEC-62. CA-DEC62-34 a CA-DEC62-41 fueron aprobados e incorporados a continuación. El historial está en [la nota DEC-62](decision-dec-62.md).

#### CA-DEC62-34

El estado efectivo de toda tarea general del MVP pertenece exclusivamente a ACTIVA, COMPLETADA o CANCELADA_DEFINITIVAMENTE.

**Estado:** CONFIRMADO. **Origen:** DEC-62, aprobación explícita del catálogo; CA-18/21 como antecedentes.

#### CA-DEC62-35

El estado efectivo de todo compromiso diario del MVP pertenece exclusivamente a PENDIENTE, COMPLETADO, CANCELADO o REPROGRAMADO.

**Estado:** CONFIRMADO. **Origen:** DEC-62; RN-04 y CA-02 como antecedentes de resoluciones.

#### CA-DEC62-36

Al crear correctamente una tarea nueva, su estado efectivo inicial es ACTIVA. No decide asignación a jornadas futuras.

**Estado:** CONFIRMADO. **Origen:** DEC-62, inicialización explícita; RF-010.

#### CA-DEC62-37

Al crear correctamente un compromiso diario nuevo, su estado efectivo inicial es PENDIENTE. Aplica al origen y la continuación de los casos ya aprobados, sin definir generación futura/recurrencias ni duplicados.

**Estado:** CONFIRMADO. **Origen:** DEC-62, inicialización explícita; CA-04/10/11; RF-027/RF-011.

#### CA-DEC62-38

Los estados de tarea y compromiso se mantienen separados: cancelar/reprogramar un compromiso de una tarea ACTIVA no cambia por sí mismo esa tarea. En el ejemplo cuantitativo aprobado, al completar la continuación, tarea y compromiso de destino se completan y el original permanece REPROGRAMADO.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-08/19; RN-11/RN-15.

#### CA-DEC62-39

Registrar avances parciales no crea un estado efectivo EN_PROGRESO en la tarea o el compromiso; cualquier estado efectivo pertenece a su catálogo y se conservan las condiciones de confirmación explícita previamente aprobadas.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-08/16; RN-15. No fija aquí otras transiciones por registrar avances.

#### CA-DEC62-40

Preparar una cancelación definitiva no crea estado efectivo EN_CANCELACIÓN ni altera estados efectivos de tarea/compromisos. Abandonar conserva esos estados; la confirmación válida aplica las transiciones aprobadas conjuntamente.

**Estado:** CONFIRMADO. **Origen:** DEC-62; CA-29/30/31/32.

#### CA-DEC62-41

Definir los catálogos no habilita automáticamente todas las combinaciones de transición. Reactivaciones y correcciones de resoluciones históricas siguen sin una transición aprobada; solo se especifican aquí las transiciones previamente confirmadas.

**Estado:** CONFIRMADO. **Origen:** DEC-62; pendientes DEC-69; RN-20/RN-28 conservan sus principios confirmados. Este criterio controla el alcance del PRD, no prescribe un comportamiento de rechazo o interfaz.

## Preguntas abiertas del bloque DEC-62

El PO confirmó que guardar una tarea asignada a una jornada abierta crea automáticamente el compromiso, sin segunda confirmación. Los criterios CA-DEC62-10 a CA-DEC62-17 fueron aprobados e incorporados en FR-3; su historial está en [la nota DEC-62](decision-dec-62.md).

Permanecen pendientes las asignaciones a fechas futuras, posibles compromisos duplicados, recurrencias, registro de avances sin compromiso previo y el alcance de incorporación formal fuera del caso aprobado; retiro y su encaje con las resoluciones; casos adicionales fuera del mecanismo de cancelación definitiva aprobado; jornada comprometida; definición exacta de ejecución frente a registro de avance; transiciones de tareas/compromisos aún no confirmadas; el catálogo ordinario de jornadas se especifica en FR-5. La relación entre finalizar tarea y resolver compromiso fuera del ejemplo cuantitativo aprobado sigue PENDIENTE, incluidos hábitos recurrentes y tareas sin métricas.

Siguen explícitamente PENDIENTES la reactivación de tareas completadas o canceladas, correcciones de resoluciones históricas, finalización de tareas sin metas cuantitativas, comportamiento particular de recurrencias, asignaciones futuras, prevención de duplicados y aspectos del ciclo de jornadas no resueltos en FR-5. Los principios ya confirmados de corrección auditada y apertura/cierre manuales se conservan, sin inventar su desarrollo.

Los demás pendientes DEC-60 a DEC-75 conservan su estado, salvo los aspectos explícitamente resueltos aquí. Fórmulas, sobrecumplimiento y cambios de meta no se infieren del ejemplo. Después se abordarán apertura, cierre y límites temporales; el orden sigue siendo recomendación de conversación.

## Límites de esta iteración

Las decisiones de este bloque no aprueban esquema de base de datos, nombres de modelos, tecnología de trazabilidad, fórmulas adicionales ni historias de implementación. El PRD no está cerrado. Las correcciones auditadas de RN-20/RN-28 conservan su vigencia; completar la continuación no cambia por sí mismo resultados históricos.

## Funcionalidad — ciclo de vida de jornadas

### FR-5 — Apertura, cierre, descanso y regularización

**Estado:** CONFIRMADO. Catálogo ordinario exhaustivo SIN_ABRIR, ABIERTA, CERRADA. Toda jornada se abre manualmente antes de cerrarse, incluida histórica, vacía o descanso. No hay cierre directo desde SIN_ABRIR. El cierre requiere confirmación manual y compromisos resueltos; resolverlos no cierra automáticamente. Jornada vacía abierta puede cerrarse sin incumplimiento. Descanso exige ABIERTA y resolución/traslado justificado previo; resulta CERRADA identificada como descanso. Históricas con compromisos y sin cierre se regularizan individualmente aun nunca abiertas, manteniendo fecha original. Corrección auditada no reabre.

La fecha de jornada se distingue del momento real de apertura/cierre. Una interfaz puede reunir el flujo, conservando las dos confirmaciones como operaciones lógicas independientes. Detalles temporales e implementación no están decididos.

**Origen:** RF-011, RF-015, RF-025, RF-028, RF-032; RN-01 a RN-06, RN-08, RN-16, RN-20, RN-23, RN-28; DEC-01, DEC-03, DEC-08, DEC-20, DEC-23, DEC-28, DEC-64. Precisiones y aprobación en [registro del bloque jornadas](jornadas-propuesta.md). No se amplía DEC-62.

**CA-JOR-01 a CA-JOR-17 CONFIRMADOS:**

#### CA-JOR-01

El estado efectivo de la jornada en el ciclo ordinario pertenece exclusivamente a SIN_ABRIR, ABIERTA o CERRADA.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-03, aprobación catálogo PO.

#### CA-JOR-02

Antes de abrir manualmente, la jornada es SIN_ABRIR, aun si tiene compromisos programados.

**Estado:** CONFIRMADO. **Origen:** DEC-01; RN-01; RF-011.

#### CA-JOR-03

La apertura manual cambia SIN_ABRIR a ABIERTA conservando los compromisos asociados.

**Estado:** CONFIRMADO. **Origen:** DEC-01; RN-01; RF-011.

#### CA-JOR-04

Abrir no resuelve ni modifica automáticamente planificación, estado o resolución de compromisos ya asociados.

**Estado:** CONFIRMADO. **Origen:** DEC-01; RN-01; FR-3, independencia aprobada en DEC-62 como antecedente.

#### CA-JOR-05

ABIERTA permite las operaciones de planificación, registro de avances y resolución previamente aprobadas, bajo sus condiciones y límites.

**Estado:** CONFIRMADO. **Origen:** RF-010/RF-011/RF-016/RF-025; RN-02/RN-04; FR-1 a FR-4.

#### CA-JOR-06

Si algún compromiso de la jornada permanece PENDIENTE, no se permite confirmar el cierre.

**Estado:** CONFIRMADO. **Origen:** RF-025; RN-03; DEC-03.

#### CA-JOR-07

Resolver todos los compromisos no cierra la jornada: permanece ABIERTA hasta confirmación manual.

**Estado:** CONFIRMADO. **Origen:** RF-025; RN-03; DEC-03, precisión PO.

#### CA-JOR-08

La confirmación manual válida de cierre de una jornada ABIERTA cambia su estado a CERRADA y conserva registro del cierre.

**Estado:** CONFIRMADO. **Origen:** RF-025; RN-03; DEC-03.

#### CA-JOR-09

Una jornada ABIERTA sin compromisos puede cerrarse mediante confirmación manual sin que esa ausencia cuente como incumplimiento.

**Estado:** CONFIRMADO. **Origen:** DEC-64, precisión PO; RF-025/RN-03.

#### CA-JOR-10

Al confirmar válidamente un día de descanso, la jornada resultante es CERRADA y queda identificada explícitamente como descanso.

**Estado:** CONFIRMADO. **Origen:** RF-015; RN-23; DEC-23, precisión PO.

#### CA-JOR-11

Antes de confirmar descanso deben estar resueltos los compromisos asumidos, incluido traslado por reprogramación con categoría, explicación y fecha destino cuando corresponda.

**Estado:** CONFIRMADO. **Origen:** RF-015/RF-026/RF-027; RN-23/RN-04 a RN-06; DEC-23.

#### CA-JOR-12

La declaración de descanso no genera por sí misma una penalización de cumplimiento.

**Estado:** CONFIRMADO. **Origen:** RF-015; RN-23; DEC-23.

#### CA-JOR-13

Una fecha pasada con compromisos asumidos y sin cierre confirmado se identifica para regularización aunque la jornada sea SIN_ABRIR.

**Estado:** CONFIRMADO. **Origen:** RF-028; RN-08; DEC-08, precisión PO.

#### CA-JOR-14

Cada jornada histórica se regulariza individualmente conservando su fecha original; los avances mantienen su fecha real.

**Estado:** CONFIRMADO. **Origen:** RF-028/RF-017; RN-08/RN-16; DEC-08/DEC-16.

#### CA-JOR-15

La regularización resuelve los compromisos pendientes y requiere confirmación manual del cierre; resolverlos no cierra automáticamente.

**Estado:** CONFIRMADO. **Origen:** RF-028/RF-025; RN-08/RN-03 a RN-06; DEC-08/DEC-03.

#### CA-JOR-16

Corregir una jornada CERRADA exige justificación y auditoría, manteniéndola CERRADA sin reapertura.

**Estado:** CONFIRMADO. **Origen:** RF-028; RN-20; DEC-20/DEC-69.

#### CA-JOR-17

Correcciones históricas aprobadas actualizan estadísticas actuales y conservan revisiones originales e historial.

**Estado:** CONFIRMADO. **Origen:** RF-032; RN-28; DEC-28/DEC-69.

### Itinerario obligatorio — criterios CONFIRMADOS

**Origen:** aprobación explícita del PO de CA-JOR-18 a CA-JOR-25, sin modificaciones.

#### CA-JOR-18

Toda jornada que se cierra ha pasado previamente por apertura manual, incluidas históricas, vacías y descansos; el ciclo ordinario es SIN_ABRIR → ABIERTA → CERRADA.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-03; RN-01/RN-03; CA-JOR-01/03/08.

#### CA-JOR-19

Si una jornada está SIN_ABRIR, no se permite confirmar directamente su cierre; debe abrirse manualmente primero.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-03; RN-01; CA-JOR-03/08.

#### CA-JOR-20

Para regularizar una histórica SIN_ABRIR con compromisos asumidos, se abre manualmente en su fecha original, se resuelven sus compromisos y se confirma cierre; la apertura posterior no cambia esa fecha.

**Estado:** CONFIRMADO. **Origen:** DEC-08; RF-028; RN-08; CA-JOR-13/14/15.

#### CA-JOR-21

Una jornada sin compromisos puede abrirse y cerrarse manualmente sin que la ausencia de compromisos se contabilice como incumplimiento. No define fórmulas ni tratamiento de días nunca abiertos.

**Estado:** CONFIRMADO. **Origen:** DEC-64; CA-JOR-09; RF-025.

#### CA-JOR-22

Solo una jornada ABIERTA permite confirmar descanso y cierre; sus compromisos deben estar resueltos o trasladados justificadamente. El resultado es CERRADA e identificado como descanso.

**Estado:** CONFIRMADO. **Origen:** DEC-23; RF-015; RN-23; CA-JOR-10/11/12.

#### CA-JOR-23

Si apertura y cierre se ofrecen en una misma interfaz, conservan dos confirmaciones manuales lógicamente independientes; confirmar apertura no confirma por sí mismo cierre ni descanso.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-03/DEC-23; RN-01/RN-03; nueva precisión PO.

#### CA-JOR-24

Puede distinguirse la fecha de la jornada del momento real de su apertura y cierre, incluso al regularizar una fecha pasada; no se registra la apertura o cierre como si hubieran ocurrido en la fecha histórica. No prescribe formato, precisión temporal ni almacenamiento.

**Estado:** CONFIRMADO. **Origen:** DEC-08; RN-08; nueva precisión PO; DEC-68 pendiente.

#### CA-JOR-25

Una corrección justificada y auditada de CERRADA no ejecuta apertura ni la cambia a ABIERTA; mantiene CERRADA conservando historial.

**Estado:** CONFIRMADO. **Origen:** DEC-20; RN-20; CA-JOR-16/17; DEC-69 pendiente.

DEC-60 está CONFIRMADA: se permite planificar en SIN_ABRIR y se exige ABIERTA para registrar avances o confirmar cumplimiento. Los criterios CA-DEC60-01 a CA-DEC60-04 fueron aprobados; su historial está en [la nota DEC-60](decision-dec-60.md). Esta aprobación no decide compromisos previos, fechas futuras o duplicados.

### FR-6 — Operaciones antes de la apertura

**Estado:** CONFIRMADO. Se permite planificar en SIN_ABRIR; registrar avances y confirmar cumplimiento requiere ABIERTA. No decide creación de compromisos antes de abrir, asignaciones futuras, duplicados ni trabajo sin compromiso.

**Origen:** DEC-60; RF-011, RF-016, RF-018, RF-025; RN-01, RN-15.

#### CA-DEC60-01

En SIN_ABRIR se permite planificar sin que esa acción abra automáticamente la jornada.

**Estado:** CONFIRMADO. **Origen:** DEC-60; RN-01; RF-011.

#### CA-DEC60-02

En SIN_ABRIR no se permite registrar avances; la operación exige apertura manual previa.

**Estado:** CONFIRMADO. **Origen:** DEC-60; RF-016; RN-01.

#### CA-DEC60-03

En SIN_ABRIR no se permite confirmar cumplimiento de compromisos o tareas de esa jornada.

**Estado:** CONFIRMADO. **Origen:** DEC-60; RN-15; RF-018/RF-025.

#### CA-DEC60-04

Tras abrir manualmente, se permiten registro de avances y confirmación de cumplimiento bajo sus reglas ya aprobadas; abrir no confirma cumplimiento por sí mismo.

**Estado:** CONFIRMADO. **Origen:** DEC-60; RN-01/RN-15; CA-JOR-03/04/05.

Siguen PENDIENTES cierre anticipado/actividad posterior, días pasados vacíos nunca abiertos, fórmulas de vacíos/descansos, alcance de correcciones, jornadas abiertas simultáneamente y medianoche/zona horaria. El PRD permanece draft; no hay estados adicionales ni implementación.

## DEC-61 — Reapertura justificada CONFIRMADA

El PO confirma poder reabrir explícitamente una jornada CERRADA para ingresar otra actividad del mismo día, registrando justificación de la acción: CERRADA → ABIERTA, sin estado adicional. Esta excepción cambia la interpretación anterior de prohibición absoluta de reapertura. CA-JOR-16/25 siguen describiendo correcciones auditadas sin reapertura automática; el ciclo ordinario de CA-JOR-18 conserva su texto con esta excepción explícita.

[La nota DEC-61](decision-dec-61.md) conserva procedencia, diferencia y preguntas abiertas. CA-DEC61-01 a CA-DEC61-04 están CONFIRMADOS por aprobación explícita del PO e incorporados a continuación. No se habilita reapertura de jornadas de fechas anteriores o cambios históricos por inferencia. La precisión posterior de descanso se documenta al final. El PRD sigue draft.

### FR-7 — Reapertura justificada del mismo día

**Estado:** CONFIRMADO. El usuario puede reabrir explícitamente una jornada CERRADA para ingresar una actividad adicional del mismo día, registrando justificación. Reabrir no es una corrección histórica automática; no se extiende a fechas anteriores por inferencia; la precisión posterior de descanso se documenta al final.

**Origen:** DEC-61, aprobación explícita PO; relación con FR-3/FR-5/FR-6 y RN-03 a RN-06. Excepción documentada respecto de prohibición absoluta previa; CA-JOR-16/25 conservan corrección sin reapertura por sí misma.

#### CA-DEC61-01

Para ingresar una actividad adicional del mismo día, el usuario puede solicitar explícitamente la reapertura de su jornada CERRADA; si se confirma válidamente, pasa a ABIERTA conservando su fecha.

**Estado:** CONFIRMADO. **Origen:** DEC-61, nueva confirmación PO; estados CA-JOR-01.

#### CA-DEC61-02

Sin justificación registrada no se permite confirmar la reapertura. No se exige categoría por inferencia; formato y validación exactos pendientes.

**Estado:** CONFIRMADO. **Origen:** DEC-61, justificación exigida por PO.

#### CA-DEC61-03

Ingresar una actividad no reabre silenciosamente: la reapertura es una acción explícita del usuario.

**Estado:** CONFIRMADO. **Origen:** DEC-61; RN-01 como antecedente de control manual.

#### CA-DEC61-04

Tras reabrir, la actividad se incorpora bajo las reglas aprobadas para ABIERTA; volver a cerrar requiere resolver compromisos y nueva confirmación manual.

**Estado:** CONFIRMADO. **Origen:** FR-3; RN-03 a RN-06; CA-JOR-05/06/07/08; coordinación propuesta para DEC-61.


### Historial de apertura, cierre y reapertura — decisión CONFIRMADA

El PO confirmó conservar cada apertura, cierre y reapertura con su momento real, la justificación de cada reapertura y todos los cierres anteriores sin reemplazarlos. Se distingue fecha de jornada de los momentos reales de acción. Origen DEC-61; antecedente CA-JOR-24/RNF-002. No se prescribe implementación.

CA-DEC61-05 a CA-DEC61-08 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-61](decision-dec-61.md). La presentación del historial y el cómputo estadístico siguen pendientes; esta decisión no amplía las reaperturas permitidas.

#### CA-DEC61-05

Cada apertura, cierre y reapertura efectivamente realizados conserva un registro distinguible de la acción y su momento real. No se fija formato ni precisión temporal.

**Estado:** CONFIRMADO. **Origen:** DEC-61, confirmación PO; CA-JOR-24.

#### CA-DEC61-06

Cada reapertura conserva la justificación correspondiente vinculada a esa acción, sin sustituir la de una reapertura anterior.

**Estado:** CONFIRMADO. **Origen:** DEC-61; CA-DEC61-02; RNF-002 como antecedente.

#### CA-DEC61-07

Reabrir o volver a cerrar no reemplaza ni elimina los registros de cierres anteriores de la misma jornada.

**Estado:** CONFIRMADO. **Origen:** DEC-61, nueva confirmación; RNF-002 como antecedente.

#### CA-DEC61-08

Tras apertura, cierre, reapertura y nuevo cierre, el historial permite distinguir las cuatro acciones con sus momentos reales y la justificación de la reapertura, conservando la fecha de jornada.

**Estado:** CONFIRMADO. **Origen:** DEC-61; CA-DEC61-01/04; CA-JOR-24.

### Retiro de descanso al reabrir — decisión CONFIRMADA

El PO confirma retirar explícitamente la marca de descanso al reabrir para agregar actividad en el caso del mismo día aprobado. Se mantienen la reapertura explícita y su justificación. El cierre anterior se conserva en historial. Efectos estadísticos siguen pendientes; la coordinación fue confirmada posteriormente y se registra al final. CA-DEC61-09 a CA-DEC61-11 fueron aprobados explícitamente e incorporados a continuación; su historial está en [la nota DEC-61](decision-dec-61.md).

#### CA-DEC61-09

En el caso aprobado del mismo día, reabrir una jornada cerrada como descanso para agregar actividad requiere retirar explícitamente la marca de descanso.

**Estado:** CONFIRMADO. **Origen:** DEC-61, respuesta explícita PO; RN-23/CA-JOR-10 como antecedentes.

#### CA-DEC61-10

La reapertura desde descanso conserva los requisitos de acción explícita y justificación; retirar la marca no abre por sí mismo una jornada silenciosamente.

**Estado:** CONFIRMADO. **Origen:** DEC-61; CA-DEC61-01/02/03.

#### CA-DEC61-11

Retirar la marca vigente de descanso no elimina el registro del cierre anterior ni los momentos y justificaciones ya conservados. No establece recálculo estadístico.

**Estado:** CONFIRMADO. **Origen:** DEC-61; CA-DEC61-05 a CA-DEC61-08.

### Consistencia del retiro de descanso y reapertura — CONFIRMADO

El PO aprueba confirmar conjuntamente el retiro explícito de descanso y la reapertura; si falla, la jornada permanece CERRADA y conserva la marca de descanso. No se prescribe mecanismo técnico. CA-DEC61-12 a CA-DEC61-14 fueron aprobados explícitamente e incorporados a continuación; el historial está en [la nota DEC-61](decision-dec-61.md). El efecto estadístico sigue pendiente.

#### CA-DEC61-12

Una confirmación válida del caso aprobado aplica conjuntamente la retirada explícita de la marca de descanso y la reapertura: el resultado es ABIERTA sin la marca vigente de descanso.

**Estado:** CONFIRMADO. **Origen:** DEC-61, nueva aprobación PO; CA-DEC61-01/09/10.

#### CA-DEC61-13

Si falla esa operación, la jornada permanece CERRADA y conserva la marca de descanso; no queda aplicada solo una de las dos acciones.

**Estado:** CONFIRMADO. **Origen:** DEC-61, garantía aprobada por PO.

#### CA-DEC61-14

La operación conjunta conserva la justificación de reapertura y los registros de cierres anteriores, sin eliminar el historial del descanso declarado.

**Estado:** CONFIRMADO. **Origen:** DEC-61; CA-DEC61-05/06/07/11.

## DEC-68 — Zona del navegador y límite del día

**Decisión CONFIRMADA:** fecha local y cambio de día a las 00:00 según zona horaria reportada por el navegador. Sustituye America/Santiago como zona fija de DEC-24/RN-24; semana desde lunes sigue vigente. Reapertura del mismo día se interpreta según esa fecha local. No se prescribe ubicación geográfica ni mecanismo técnico. Cambios de zona e historial, trabajo que cruza medianoche y fallback siguen pendientes.

CA-DEC68-01 a CA-DEC68-04 fueron aprobados explícitamente e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md). Los criterios previos conservan su historial de aprobación, con la precisión de zona aquí registrada como prevalente.

### FR-8 — Día calendario según zona horaria del navegador

**Estado:** CONFIRMADO. La fecha local y el límite de día se determinan según la zona horaria reportada por el navegador; el cambio de día ocurre a las 00:00 locales. La reapertura del mismo día exige que la fecha de jornada coincida con el día local actual. Se conservan momentos reales de acciones y avances; no se decide reinterpretación histórica tras cambio de zona.

**Origen:** DEC-68, precisión posterior de DEC-24/RN-24; RN-16; CA-JOR-24; CA-DEC61-01/05/08. Semana desde lunes conserva vigencia; no se prescribe mecanismo técnico.

#### CA-DEC68-01

La fecha local utilizada para identificar el día del usuario se determina usando la zona horaria reportada por su navegador, sin fijarla a America/Santiago.

**Estado:** CONFIRMADO. **Origen:** DEC-68 y precisión posterior de DEC-24/RN-24.

#### CA-DEC68-02

El día calendario cambia a las 00:00 locales de la zona del navegador.

**Estado:** CONFIRMADO. **Origen:** DEC-68, aprobación PO del límite propuesto.

#### CA-DEC68-03

La reapertura de DEC-61 solo se habilita si la fecha de jornada coincide con el día local actual; después de medianoche no se habilita por esa regla para la fecha anterior.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC61-01; CA-JOR-13/20 como antecedentes históricos.

#### CA-DEC68-04

Aperturas, cierres, reaperturas y avances conservan sus momentos reales; aplicar la zona del navegador no permite registrar nuevas acciones como si hubieran ocurrido en una fecha histórica.

**Estado:** CONFIRMADO. **Origen:** CA-JOR-24; CA-DEC61-05/08; RN-16. Regla para reinterpretar historial tras cambios de zona queda pendiente.


### Cambio de zona — conservación histórica CONFIRMADA

El PO aprueba conservar las fechas originales del historial al cambiar zona del navegador; la nueva zona determina el día actual sin trasladar automáticamente jornadas o avances anteriores. El tratamiento de jornadas ya abiertas y el momento de adopción siguen pendientes. CA-DEC68-05 a CA-DEC68-07 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md).

#### CA-DEC68-05

Cambiar la zona reportada por el navegador no modifica las fechas originales de jornadas ni avances históricos.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación PO; RN-08/RN-16 como antecedentes.

#### CA-DEC68-06

El cambio de zona no traslada automáticamente compromisos, jornadas o avances históricos a otra fecha. No determina qué hacer con jornadas abiertas durante el cambio.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC62-06/09 como antecedentes de conservación. La referencia a compromisos preserva el vínculo histórico con jornada, sin definir asignación futura.

#### CA-DEC68-07

La nueva zona se usa para determinar el día local actual, manteniendo el historial con sus fechas originales. No fija el instante de adopción del cambio ni su efecto en jornadas abiertas.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-01/02.

### Jornada abierta ante cambio de zona — precisión CONFIRMADA

El PO aprueba que una jornada ya ABIERTA conserve hasta su cierre la fecha y zona con las que se abrió, aunque cambie la zona del navegador. La nueva zona determina el día actual para siguientes jornadas; no reasigna automáticamente la abierta. Esta precisión contextualiza CA-DEC68-07 sin reemplazarlo. Atribución de nuevos avances durante el cambio y coincidencias siguen pendientes.

CA-DEC68-08 a CA-DEC68-10 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md).

#### CA-DEC68-08

Si cambia la zona del navegador mientras una jornada está ABIERTA, esa jornada conserva hasta su cierre la fecha y zona con las que se abrió.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación PO; CA-DEC68-05/06.

#### CA-DEC68-09

Cambiar la zona no cierra, reabre ni cambia automáticamente el estado de esa jornada; el cierre conserva las condiciones y confirmación manual previamente aprobadas.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-JOR-07/08/18.

#### CA-DEC68-10

La nueva zona determina el día local actual para las siguientes jornadas, sin reasignar por ello la jornada que ya estaba ABIERTA.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-01/02/07 y nueva precisión PO.

### Atribución de nuevos avances tras cambio de zona — CONFIRMADO

El PO aprueba atribuir nuevos avances a su fecha real según la nueva zona del navegador, aun vinculados a compromisos de una jornada abierta con zona anterior. No cambia por ello la fecha/zona de jornada o fecha de compromiso, ni reasigna avances históricos. Se distingue día de esfuerzo del día de compromiso.

CA-DEC68-11 a CA-DEC68-13 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md). Adopción exacta de zona y reparto de ejecuciones que cruzan medianoche siguen pendientes.

#### CA-DEC68-11

Después de adoptar la nueva zona del navegador, un nuevo avance se atribuye a su fecha real de ejecución en esa zona, aunque el compromiso pertenezca a una jornada abierta con zona anterior.

**Estado:** CONFIRMADO. **Origen:** DEC-68, confirmación explícita PO; RN-16; RF-017.

#### CA-DEC68-12

Registrar ese avance no cambia la fecha o zona conservada de la jornada abierta ni la fecha de su compromiso.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-08/10; CA-DEC62-06.

#### CA-DEC68-13

El esfuerzo del nuevo avance se atribuye a su fecha real y no se duplica para atribuirlo también al día del compromiso; mantiene el vínculo con el compromiso y la tarea.

**Estado:** CONFIRMADO. **Origen:** DEC-68; RN-16/RN-26; RF-017/RF-019; CA-DEC62-09.

### Sesión que cruza medianoche — precisión CONFIRMADA

El PO decide atribuir toda la sesión a su fecha de inicio. Ejemplo: 23:40–00:20, 40 minutos íntegros en la fecha de inicio. No se divide automáticamente entre días. Se conservan momentos reales de ejecución; esta convención precisa la atribución de esfuerzo de RN-16/CA-DEC68-11/13, sin alterar momentos o fechas de jornada.

CA-DEC68-14 a CA-DEC68-16 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md). Cambios de zona dentro de una sesión e inicio desconocido siguen pendientes; no se prescribe captura técnica.

#### CA-DEC68-14

Una sesión que comienza antes de medianoche y termina después se atribuye completamente a su fecha de inicio, sin dividirla automáticamente entre fechas.

**Estado:** CONFIRMADO. **Origen:** DEC-68, elección explícita del PO; precisión de RN-16/RF-017.

#### CA-DEC68-15

En el ejemplo 23:40–00:20, los 40 minutos se atribuyen a la fecha de inicio; no se atribuyen 20 minutos al día siguiente ni 40 minutos adicionales a la fecha de término.

**Estado:** CONFIRMADO. **Origen:** DEC-68; RN-26/RF-019; CA-DEC68-13.

#### CA-DEC68-16

La atribución a la fecha de inicio conserva los momentos reales de inicio y término y los vínculos con tarea/compromiso; no cambia la fecha de jornada por terminar después de medianoche.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-04/12/13; CA-JOR-24.

### Cambio de zona durante una sesión — precisión CONFIRMADA

El PO aprueba que la sesión ya iniciada conserve la fecha de inicio calculada con la zona vigente al comenzar, aunque cambie la zona durante el trabajo. Las sesiones nuevas usan la nueva zona. Esto precisa CA-DEC68-11 para sesiones en curso, sin reasignar historial ni dividir esfuerzo. CA-DEC68-17 a CA-DEC68-19 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md).

#### CA-DEC68-17

Si cambia la zona del navegador durante una sesión, su fecha de atribución sigue siendo la fecha de inicio calculada en la zona vigente al comenzar, aunque termine o se registre después del cambio.

**Estado:** CONFIRMADO. **Origen:** DEC-68, aprobación explícita PO; CA-DEC68-14/16.

#### CA-DEC68-18

Las sesiones iniciadas después de adoptar la nueva zona calculan su fecha de inicio en esa nueva zona, sin cambiar la fecha de sesiones anteriores.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-05/11 y nueva precisión PO.

#### CA-DEC68-19

Cambiar de zona durante una sesión no divide ni duplica su esfuerzo: la sesión completa conserva una única fecha de atribución y sus momentos reales.

**Estado:** CONFIRMADO. **Origen:** DEC-68; RN-26; CA-DEC68-13/14/15/16.

### Adopción automática de zona — CONFIRMADO

Al detectar una zona distinta reportada por el navegador, se adopta para nuevas jornadas y sesiones desde ese momento sin confirmación adicional. Las jornadas abiertas y sesiones iniciadas conservan sus referencias temporales ya aprobadas y no se reasigna historial. No se define mecanismo/frecuencia de detección ni fallback ante zona inválida.

CA-DEC68-20 a CA-DEC68-22 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md).

#### CA-DEC68-20

Cuando la aplicación detecta una zona distinta válida reportada por el navegador, la adopta para nuevas jornadas y sesiones desde ese momento, sin confirmación adicional del usuario.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación explícita PO; CA-DEC68-01/10/18.

#### CA-DEC68-21

Adoptar la nueva zona conserva fecha y zona de las jornadas ya abiertas hasta cierre y la fecha de inicio calculada con la zona original de sesiones ya iniciadas.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-08/17.

#### CA-DEC68-22

La adopción automática no cambia fechas históricas, no cierra/reabre jornadas ni divide o duplica esfuerzo registrado.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-05/06/09/19.

### Zona inválida o ausente — decisión CONFIRMADA

Si el navegador no informa una zona válida, se conserva la última zona válida conocida. Si no existe ninguna previa, se solicita al usuario seleccionar una, sin zona fija impuesta por defecto. Origen DEC-68, aprobación explícita PO. La adopción automática posterior de zona válida conserva sus condiciones aprobadas; operaciones antes de selección siguen pendientes.

CA-DEC68-23 a CA-DEC68-25 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md).

#### CA-DEC68-23

Si el navegador no informa una zona válida y existe una última zona válida conocida, se conserva esa zona para determinar fecha y día local.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación PO; CA-DEC68-01/02/20.

#### CA-DEC68-24

Si no hay zona válida del navegador ni una última zona válida conocida, se solicita al usuario seleccionar una zona válida, sin imponer una fija por defecto.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación PO; precisión DEC-24/RN-24.

#### CA-DEC68-25

Cuando posteriormente se detecta una zona válida distinta del navegador, se aplica la adopción automática ya aprobada, preservando historial y referencias de jornadas/sesiones iniciadas.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-20/21/22.

### Ausencia de toda zona válida — CONFIRMADO

El PO aprueba consultar información existente sin zona válida disponible, pero exige seleccionar una antes de operaciones dependientes de fecha, como abrir jornadas o registrar avances. Si existe última zona válida, se conserva el respaldo aprobado; esta restricción no lo anula. No se inventa zona por defecto ni se completa automáticamente la clasificación de todas las operaciones.

CA-DEC68-26 a CA-DEC68-28 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-68](decision-dec-68.md). La selección no sustituye otras condiciones funcionales. PRD draft.

#### CA-DEC68-26

Sin zona válida del navegador ni última zona válida conocida, el usuario puede consultar información existente sin que se le imponga una zona fija por defecto.

**Estado:** CONFIRMADO. **Origen:** DEC-68, nueva aprobación PO; CA-DEC68-23/24.

#### CA-DEC68-27

En esa situación, abrir jornadas o registrar avances requiere seleccionar previamente una zona válida; intentar esas operaciones no las aplica usando una zona supuesta.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC68-24; RN-01/RN-16 como antecedentes.

#### CA-DEC68-28

Después de seleccionar una zona válida, pueden realizarse las operaciones dependientes de fecha bajo sus demás condiciones ya aprobadas; la selección por sí sola no abre una jornada ni registra avances.

**Estado:** CONFIRMADO. **Origen:** DEC-68; CA-DEC60-02/04; CA-JOR-03/04.

## DEC-64 — Días pasados vacíos nunca abiertos

**Decisión CONFIRMADA:** una fecha pasada nunca abierta y sin compromisos asumidos no exige regularización ni se considera incumplimiento automáticamente. No se confunde con días que tuvieron compromisos luego resueltos/retirados; no implica apertura/cierre automático o descanso supuesto. Las jornadas vacías abiertas sin cerrar y fórmulas estadísticas permanecen pendientes.

CA-DEC64-01 a CA-DEC64-04 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-64](decision-dec-64.md).

### FR-9 — Fechas pasadas vacías nunca abiertas

**Estado:** CONFIRMADO. Una fecha pasada nunca abierta y sin compromisos asumidos no exige regularización ni es incumplimiento automático. No borra historial ni declara cierre/descanso por inferencia. Origen DEC-64; relación con RN-08/RN-19/RN-25 y CA-JOR-13. Fórmulas y vacías abiertas sin cerrar pendientes.

#### CA-DEC64-01

Una fecha pasada nunca abierta y sin compromisos asumidos no se identifica como obligatoria de regularización.

**Estado:** CONFIRMADO. **Origen:** DEC-64, aprobación PO; contraste RN-08/CA-JOR-13.

#### CA-DEC64-02

Ese día no se clasifica automáticamente como incumplimiento por ausencia de apertura o cierre. No fija fórmulas ni denominadores.

**Estado:** CONFIRMADO. **Origen:** DEC-64, aprobación PO; DEC-63 pendiente.

#### CA-DEC64-03

Resolver, cancelar, reprogramar o retirar compromisos no convierte una fecha que los tuvo en un día sin compromisos asumidos a efectos de esta excepción.

**Estado:** CONFIRMADO. **Origen:** DEC-64; RN-19/RN-25; CA-JOR-13; RF-035.

#### CA-DEC64-04

Aplicar esta excepción no abre/cierra la jornada automáticamente ni declara descanso; no agrega un estado efectivo adicional.

**Estado:** CONFIRMADO. **Origen:** DEC-64; RN-01/RN-03; CA-JOR-01/03/07.


### Jornada abierta vacía pendiente de cierre — CONFIRMADO

Una jornada ABIERTA sin compromisos exige cierre manual individual incluso pasada su fecha, sin considerarse incumplimiento de tareas. Conserva fecha original y momento real de cierre. La métrica de consistencia y su relación con bloqueo periódico siguen pendientes; no se amplía RN-27 por inferencia.

CA-DEC64-05 a CA-DEC64-07 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-64](decision-dec-64.md).

#### CA-DEC64-05

Una jornada ABIERTA sin compromisos no se cierra automáticamente ni queda dispensada de cierre manual.

**Estado:** CONFIRMADO. **Origen:** DEC-64, aprobación PO; CA-JOR-07/09/21.

#### CA-DEC64-06

Si su fecha ya pasó y sigue ABIERTA, requiere cierre manual individual conservando su fecha original y distinguiendo el momento real de cierre.

**Estado:** CONFIRMADO. **Origen:** DEC-64; RN-08 como antecedente de fecha original; CA-JOR-24.

#### CA-DEC64-07

Cerrar esa jornada vacía no cuenta como incumplimiento de tareas; no define su efecto en consistencia de cierres.

**Estado:** CONFIRMADO. **Origen:** DEC-64; CA-JOR-09/21; DEC-63 pendiente.

## DEC-27 — Ampliación del bloqueo periódico CONFIRMADA

El PO aprueba que toda jornada ABIERTA dentro del período impida confirmar el cierre de la revisión semanal/mensual, aunque esté vacía o tenga sus compromisos resueltos. Se amplía explícitamente RN-27/DEC-27 conservando el bloqueo por fechas con compromisos y sin cierre, incluso SIN_ABRIR. No se confunde cierre de revisión con consulta o preparación de reflexión. Días nunca abiertos sin compromisos conservan excepción CA-DEC64-01.

CA-DEC27-01 a CA-DEC27-03 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-27](decision-dec-27.md). Métricas y otras condiciones del cierre periódico siguen pendientes; no hay cierre automático.

### FR-10 — Bloqueo del cierre de revisiones periódicas

**Estado:** CONFIRMADO. No se permite confirmar cierre de revisión semanal/mensual si quedan jornadas ABIERTAS del período, aunque vacías o con compromisos resueltos. Se conserva bloqueo de fechas con compromisos sin cierre incluso SIN_ABRIR. Cierre periódico sigue manual. Origen DEC-27; RF-029/RF-031; RN-10/RN-27, con ampliación explícita PO. No prescribe bloqueo de consulta ni fórmulas.

#### CA-DEC27-01

Si existe una jornada ABIERTA con fecha dentro del período, no se permite confirmar cierre de su revisión semanal o mensual, aunque tenga cero compromisos o todos resueltos.

**Estado:** CONFIRMADO. **Origen:** DEC-27, ampliación explícita RN-27; RF-031; CA-DEC64-05/06.

#### CA-DEC27-02

La ampliación conserva el bloqueo por jornadas del período con compromisos asumidos y sin cierre, incluso SIN_ABRIR; no se restringe el filtro solo a ABIERTA.

**Estado:** CONFIRMADO. **Origen:** RN-27/DEC-27; RF-031; CA-JOR-13/15/20.

#### CA-DEC27-03

Cerrar las jornadas bloqueantes elimina ese motivo de bloqueo, pero no cierra automáticamente la revisión ni dispensa su confirmación manual y demás condiciones aprobadas.

**Estado:** CONFIRMADO. **Origen:** DEC-27; RN-10; RF-029/RF-031; DEC-10.


### Jornadas abiertas simultáneamente — decisión CONFIRMADA

El PO permite abrir manualmente la jornada actual aunque queden jornadas anteriores ABIERTAS. No cierra ni modifica automáticamente las anteriores: mantienen cierre individual y bloqueo de revisión periódica correspondiente. Origen DEC-01/DEC-08/DEC-27. No se aprueban duplicados de jornada/compromiso o asignaciones futuras.

CA-JOR-26 a CA-JOR-28 fueron aprobados e incorporados a continuación; el historial está en [la nota jornadas](jornadas-propuesta.md). No se añaden estados ni implementación.

#### CA-JOR-26

La presencia de jornadas anteriores ABIERTAS no impide abrir manualmente la jornada actual bajo las demás condiciones aprobadas.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-08, nueva aprobación PO; CA-JOR-03; FR-6/FR-8.

#### CA-JOR-27

Abrir la jornada actual no cierra ni modifica automáticamente estado, fecha o compromisos de jornadas anteriores abiertas.

**Estado:** CONFIRMADO. **Origen:** DEC-01/DEC-08; RN-08; CA-JOR-07/14.

#### CA-JOR-28

Cada jornada anterior abierta conserva obligación de cierre manual individual y bloquea la confirmación del cierre de su revisión periódica correspondiente mientras siga abierta.

**Estado:** CONFIRMADO. **Origen:** DEC-08/DEC-27; CA-DEC27-01/02; CA-DEC64-06.

## DEC-65 — Categorías de justificación CONFIRMADAS

Lista inicial para cancelar/reprogramar compromisos: Falta de tiempo; Cambio de prioridad; Dependencia o bloqueo; Salud o descanso; Imprevisto personal; Error de planificación; Otro. La explicación textual sigue obligatoria. Origen DEC-65 y RF-026/RN-05/DEC-05.

No se extiende requisito de categoría a otras acciones por inferencia; Salud o descanso no reemplaza declaración de descanso. CA-DEC65-01 a CA-DEC65-03 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-65](decision-dec-65.md). Validación detallada/personalización pendientes.

### FR-11 — Categorías iniciales para justificar compromisos

**Estado:** CONFIRMADO. Cancelar/reprogramar compromisos exige categoría de la lista inicial aprobada y explicación textual. Origen DEC-65; RF-026; RN-05/DEC-05. No extiende categorías a otras acciones ni convierte Salud o descanso en declaración de descanso. Validación textual detallada pendiente.

#### CA-DEC65-01

Al cancelar o reprogramar un compromiso, se ofrece la lista inicial aprobada: Falta de tiempo, Cambio de prioridad, Dependencia o bloqueo, Salud o descanso, Imprevisto personal, Error de planificación y Otro.

**Estado:** CONFIRMADO. **Origen:** DEC-65, aprobación explícita PO; RF-026; RN-05.

#### CA-DEC65-02

No se confirma cancelación o reprogramación de un compromiso sin seleccionar categoría y aportar explicación textual, incluida categoría Otro. No se fija longitud ni validación detallada todavía.

**Estado:** CONFIRMADO. **Origen:** DEC-65; DEC-05; RF-026; RN-05.

#### CA-DEC65-03

Seleccionar Salud o descanso solo clasifica la justificación del compromiso; no declara descanso ni cierra la jornada automáticamente.

**Estado:** CONFIRMADO. **Origen:** DEC-65; RN-23; CA-JOR-10/11/22.


### Validación textual de justificación — CONFIRMADA

El PO aprueba rechazar explicaciones vacías o de solo espacios para cancelar/reprogramar compromisos, sin longitud mínima adicional. No se extiende por inferencia a otras acciones. CA-DEC65-04 a CA-DEC65-06 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-65](decision-dec-65.md). PRD draft.

#### CA-DEC65-04

No se permite confirmar cancelación o reprogramación de compromiso con explicación vacía.

**Estado:** CONFIRMADO. **Origen:** DEC-65, nueva aprobación PO; RN-05/RF-026; CA-DEC65-02.

#### CA-DEC65-05

Una explicación compuesta solo por espacios se considera inválida, aun con categoría seleccionada.

**Estado:** CONFIRMADO. **Origen:** DEC-65, nueva aprobación PO; RN-05.

#### CA-DEC65-06

Una explicación con al menos un carácter distinto de espacio no se rechaza por longitud mínima adicional; categoría, destino y demás condiciones siguen aplicándose.

**Estado:** CONFIRMADO. **Origen:** DEC-65; CA-DEC65-02; RN-06/RF-027.

### Justificación en cancelación definitiva, reapertura y corrección — CONFIRMADA

El PO aprueba texto no vacío ni solo espacios, sin longitud mínima adicional y sin exigir categoría en esas tres acciones. Los compromisos cancelados/reprogramados mantienen categoría y texto propios, incluso dentro de cancelación definitiva. El alcance autorizado de reapertura y correcciones no se amplía por validar justificaciones.

CA-DEC65-07 a CA-DEC65-10 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-65](decision-dec-65.md). PRD draft.

#### CA-DEC65-07

Confirmar cancelación definitiva de tarea exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; mantiene las demás condiciones aprobadas.

**Estado:** CONFIRMADO. **Origen:** DEC-65, aprobación PO; CA-DEC62-22/28/31.

#### CA-DEC65-08

Confirmar reapertura autorizada de jornada exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; no amplía el alcance de reapertura.

**Estado:** CONFIRMADO. **Origen:** DEC-65; CA-DEC61-01/02.

#### CA-DEC65-09

Una corrección auditada permitida exige justificación no vacía ni solo espacios, sin categoría ni longitud mínima adicional; auditoría y alcance pendiente se conservan.

**Estado:** CONFIRMADO. **Origen:** DEC-65; RN-20; CA-JOR-16/25; DEC-69 pendiente.

#### CA-DEC65-10

La ausencia de categoría en la justificación de cancelación definitiva no dispensa categoría y explicación para cada compromiso que se prepare cancelar dentro del procedimiento.

**Estado:** CONFIRMADO. **Origen:** DEC-65; RN-05; CA-DEC62-27/28; CA-DEC65-02.

## DEC-69 — Ámbitos de corrección histórica CONFIRMADOS

El PO confirma poder corregir tiempo registrado, resultado de compromiso y justificación en jornadas históricas CERRADAS. Se mantiene corrección justificada/auditada sin reapertura, historial conservado y estadísticas actuales actualizadas sin reemplazar revisiones originales. No aprueba todas las transiciones de resultados ni efectos automáticos sobre tareas.

CA-DEC69-01 a CA-DEC69-04 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-69](decision-dec-69.md). El PRD permanece draft.

### FR-12 — Correcciones históricas auditadas

**Estado:** CONFIRMADO. Ámbitos: tiempo registrado, resultado de compromiso y justificación histórica, con justificación y auditoría sin reapertura. Conservar anterior/nuevo e historial; actualizar estadísticas actuales manteniendo revisiones originales. Transiciones y consecuencias concretas todavía pendientes. Origen DEC-69; RF-028/RF-032; RN-20/RN-28; RNF-002; CA-DEC65-09.

#### CA-DEC69-01

El procedimiento de corrección de una jornada histórica CERRADA contempla corregir tiempo registrado sin reabrirla, con justificación y auditoría. Límites del nuevo valor y efectos cuantitativos concretos quedan pendientes.

**Estado:** CONFIRMADO. **Origen:** DEC-69, alcance aprobado; RF-028; RN-20; CA-JOR-16/25.

#### CA-DEC69-02

El procedimiento contempla corregir el resultado de un compromiso histórico, con justificación y auditoría sin reapertura; la aprobación de este ámbito no habilita todas las transiciones ni dejar compromisos PENDIENTES por inferencia.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-20; CA-DEC62-41.

#### CA-DEC69-03

El procedimiento contempla corregir una justificación histórica, distinguiéndola de la justificación obligatoria de la acción de corrección. No sustituye silenciosamente el valor previo.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-20; CA-DEC65-09.

#### CA-DEC69-04

Cada corrección aplicada conserva trazabilidad de valor anterior y nuevo con la justificación de la acción, mantiene CERRADA y actualiza estadísticas actuales conservando revisiones originales e historial. No fija mecanismo técnico.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-20/RN-28; RNF-002; CA-JOR-16/17; CA-DEC65-09.


### Corrección de compromiso COMPLETADO erróneo — CONFIRMADA

El PO aprueba COMPLETADO → CANCELADO o REPROGRAMADO en corrección histórica, con categoría y explicación, justificación de corrección y auditoría sin reapertura. REPROGRAMADO conserva fecha destino obligatoria; creación/reutilización/alteración del compromiso de destino y efecto en tarea siguen pendientes. No se aprueban otras transiciones.

CA-DEC69-05 a CA-DEC69-07 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-69](decision-dec-69.md). Se conservan valores anteriores/nuevos y revisiones originales. PRD draft.

#### CA-DEC69-05

Un compromiso histórico COMPLETADO por error puede corregirse a CANCELADO mediante corrección justificada/auditada, con categoría y explicación para la resolución, sin reabrir la jornada.

**Estado:** CONFIRMADO. **Origen:** DEC-69, aprobación explícita PO; RN-05/RN-20; CA-DEC69-02/04.

#### CA-DEC69-06

Puede corregirse de COMPLETADO erróneo a REPROGRAMADO con categoría, explicación y fecha destino, por el procedimiento auditado sin reapertura; el tratamiento del compromiso de destino permanece pendiente y no se infiere.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-05/RN-06/RN-20; RF-026/RF-027.

#### CA-DEC69-07

La corrección conserva el resultado previo y el nuevo, con justificación/auditoría, actualiza estadísticas actuales según reglas aprobadas y conserva revisiones originales e historial.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-28; CA-DEC69-04; CA-JOR-17.

### Destino de corrección a REPROGRAMADO — precisión CONFIRMADA

Crear continuación vinculada a la misma tarea si no existe correspondiente en destino. Si hay compromiso potencialmente coincidente, mostrarlo y solicitar decisión explícita, sin duplicar/modificar silenciosamente. Origen DEC-69, aprobación PO; relación RN-06/RN-11/RN-26 y DEC-67. Identificación y resolución concretas de coincidencias, estados de destino y consistencia conjunta ante fallos/abandono siguen pendientes.

CA-DEC69-08 a CA-DEC69-10 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-69](decision-dec-69.md). No se amplían reglas generales de fechas futuras, recurrencias ni cálculo de restantes.

#### CA-DEC69-08

Al corregir un compromiso a REPROGRAMADO, si no existe una continuación correspondiente en destino, se crea una vinculada a la misma tarea y al origen de la reprogramación. Fecha destino sigue obligatoria; identificación de correspondencia pendiente.

**Estado:** CONFIRMADO. **Origen:** DEC-69, aprobación PO; RN-06/RN-11; CA-DEC62-01/09; DEC-67 pendiente.

#### CA-DEC69-09

Si existe un compromiso potencialmente coincidente, se presenta al usuario y se solicita decisión explícita antes de modificarlo o crear un duplicado. No se selecciona automáticamente una forma de resolver la coincidencia.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-26 como antecedente; DEC-67 pendiente.

#### CA-DEC69-10

La gestión del destino no duplica avances previos ni altera silenciosamente el compromiso coincidente; conserva identidad de tarea y trazabilidad de origen/destino.

**Estado:** CONFIRMADO. **Origen:** DEC-69; RN-11/RN-26; CA-DEC62-06/09.

### Corrección y destino conjuntos — CONFIRMADO

El PO aprueba confirmar conjuntamente la corrección del origen a REPROGRAMADO y creación/vinculación del destino. Coincidencia no resuelta impide aplicar; abandonar o fallar no deja cambios parciales de esta operación. No selecciona mecanismo técnico ni define automáticamente las alternativas ante coincidencia.

CA-DEC69-11 a CA-DEC69-14 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-69](decision-dec-69.md). DEC-67 conserva identificación/resolución pendiente; PRD draft.

#### CA-DEC69-11

La confirmación válida aplica conjuntamente la corrección del origen a REPROGRAMADO y la creación o vinculación correspondiente del destino; no se confirma solo una parte.

**Estado:** CONFIRMADO. **Origen:** DEC-69, aprobación PO; CA-DEC69-06/08/09.

#### CA-DEC69-12

Si hay una coincidencia pendiente de decisión explícita, la corrección del origen y sus cambios de destino no se aplican. No se decide por defecto reutilizar, fusionar o reemplazar el candidato.

**Estado:** CONFIRMADO. **Origen:** DEC-69; CA-DEC69-09; DEC-67 pendiente.

#### CA-DEC69-13

Abandonar este procedimiento sin confirmar no aplica los cambios preparados al origen o destino, ni crea una continuación parcial.

**Estado:** CONFIRMADO. **Origen:** DEC-69, garantía aprobada PO.

#### CA-DEC69-14

Si falla la aplicación conjunta, no quedan parcialmente aplicadas la corrección del origen o la creación/vinculación de destino de esa operación. No se prescribe mecanismo técnico.

**Estado:** CONFIRMADO. **Origen:** DEC-69, garantía aprobada PO; RN-12/RNF-003 como antecedentes propuestos, sin promoverlos en bloque.

## DEC-67 — Definición inicial de coincidencia CONFIRMADA

Otro compromiso de la misma tarea en la fecha de destino es posible coincidencia; se muestra su estado antes de decidir. No equivale a fusionar, reemplazar o reutilizar automáticamente. Origen DEC-67, aprobación explícita PO; contexto de corrección a REPROGRAMADO DEC-69. Opciones por estado, múltiples candidatos, duplicados generales y recurrencias siguen pendientes.

CA-DEC67-01 a CA-DEC67-03 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-67](decision-dec-67.md).

### FR-13 — Identificación de coincidencias en destino

**Estado:** CONFIRMADO. En el destino de corrección a REPROGRAMADO, otro compromiso de la misma tarea en esa fecha es posible coincidencia; mostrar su estado y requerir decisión explícita sin modificación automática. Origen DEC-67; CA-DEC69-09/12; RN-26 como antecedente. Opciones por estado, múltiples candidatos, recurrencias y duplicados generales siguen pendientes.

#### CA-DEC67-01

Al evaluar el destino del caso aprobado, otro compromiso de la misma tarea en esa fecha se identifica como posible coincidencia.

**Estado:** CONFIRMADO. **Origen:** DEC-67, aprobación PO; CA-DEC69-09/12.

#### CA-DEC67-02

Antes de pedir decisión explícita sobre la coincidencia, se muestra el estado efectivo del compromiso candidato. No se fijan opciones por estado todavía.

**Estado:** CONFIRMADO. **Origen:** DEC-67; CA-DEC69-09.

#### CA-DEC67-03

Encontrar una coincidencia no fusiona, sustituye, reutiliza o modifica automáticamente el candidato ni crea un duplicado silenciosamente; mantiene el bloqueo de aplicación mientras falte decidir.

**Estado:** CONFIRMADO. **Origen:** DEC-67; CA-DEC69-09/12; RN-26.


### Candidato PENDIENTE — opciones CONFIRMADAS

El PO aprueba decisión explícita de vincular candidato PENDIENTE como continuación sin sumar trabajo automáticamente o cambiar fecha destino. No crea duplicado silenciosamente ni presupone modificar planificación del candidato. Candidatos resueltos/múltiples y fechas admisibles siguen pendientes.

CA-DEC67-04 a CA-DEC67-06 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-67](decision-dec-67.md). Se conserva aplicación conjunta origen/destino cuando corresponde, sin implementación.

#### CA-DEC67-04

Ante candidato PENDIENTE de la misma tarea en destino, se ofrecen decisiones explícitas de vincularlo como continuación o cambiar fecha destino, sin elegir por el usuario.

**Estado:** CONFIRMADO. **Origen:** DEC-67, nueva aprobación PO; CA-DEC67-01/02/03.

#### CA-DEC67-05

Elegir vincular el candidato no crea otro compromiso ni suma automáticamente trabajo, metas o avances al candidato; mantiene la trazabilidad de continuación. No se prescribe recalcular su planificación.

**Estado:** CONFIRMADO. **Origen:** DEC-67; RN-26; CA-DEC69-09/10.

#### CA-DEC67-06

Elegir cambiar la fecha mantiene pendiente la aplicación hasta definir un destino y evaluar posibles coincidencias en esa fecha; no modifica silenciosamente el candidato anterior.

**Estado:** CONFIRMADO. **Origen:** DEC-67; RN-06; CA-DEC69-11/12.

### Candidatos resueltos — CONFIRMADO

El PO aprueba mostrar COMPLETADOS/CANCELADOS/REPROGRAMADOS como antecedentes, sin convertirlos en continuación pendiente. Se exige otro destino ante ese candidato; corregir su resultado requiere procedimiento separado DEC-69 y sus reglas. Varios candidatos con estados mixtos quedan pendientes.

CA-DEC67-07 a CA-DEC67-09 fueron aprobados e incorporados a continuación; el historial está en [la nota DEC-67](decision-dec-67.md). No amplía fechas admisibles o recurrencias.

#### CA-DEC67-07

Un candidato COMPLETADO, CANCELADO o REPROGRAMADO se presenta con su estado como antecedente; no se ofrece convertirlo en continuación PENDIENTE dentro del flujo.

**Estado:** CONFIRMADO. **Origen:** DEC-67, nueva aprobación PO; CA-DEC67-02; catálogo CA-DEC62-35.

#### CA-DEC67-08

Ante ese candidato resuelto, se exige elegir otro destino y evaluar sus coincidencias antes de aplicar la operación; el antecedente conserva su resultado. No define varios candidatos mixtos.

**Estado:** CONFIRMADO. **Origen:** DEC-67; CA-DEC67-06; CA-DEC69-12.

#### CA-DEC67-09

Modificar el antecedente resuelto requiere un procedimiento de corrección separado, justificado/auditado y dentro de las transiciones aprobadas; elegir destino no lo corrige ni reabre silenciosamente.

**Estado:** CONFIRMADO. **Origen:** DEC-67; DEC-69; RN-20; CA-DEC69-01 a CA-DEC69-07.

### Múltiples candidatos de destino — CONFIRMADO

El PO aprueba mostrar todos los candidatos con su estado, seleccionar explícitamente uno PENDIENTE como continuación y conservar resueltos como antecedentes. Si no hay PENDIENTE, cambiar destino. Estados mixtos no impiden elegir un PENDIENTE distinto; no modificar no seleccionados ni fusionar automáticamente.

CA-DEC67-10 a CA-DEC67-12 fueron aprobados; véase [la nota DEC-67](decision-dec-67.md). No define creación general de duplicados ni recurrencias.

#### CA-DEC67-10

Si hay varios candidatos de la misma tarea y fecha destino, se muestran todos con su estado antes de decidir.

**Estado:** CONFIRMADO. **Origen:** DEC-67, nueva aprobación PO; CA-DEC67-01/02.

#### CA-DEC67-11

Si existe al menos un candidato PENDIENTE, el usuario puede seleccionar explícitamente uno como continuación; no se elige ni fusiona automáticamente y los demás no se modifican por seleccionarlo.

**Estado:** CONFIRMADO. **Origen:** DEC-67; CA-DEC67-04/05.

#### CA-DEC67-12

Los candidatos resueltos permanecen antecedentes no elegibles como continuación; si no existe ningún PENDIENTE, se exige cambiar destino. Un resuelto no impide seleccionar otro PENDIENTE.

**Estado:** CONFIRMADO. **Origen:** DEC-67; CA-DEC67-07/08; precisión para estados mixtos.

### Fechas admisibles para reprogramación ordinaria — CONFIRMADO

El PO aprueba fecha local actual o posterior como destino elegible, no pasada; fecha actual según zona válida adoptada DEC-68. No incorporar a jornadas CERRADAS: si es el mismo día, requiere reapertura explícita autorizada con justificación antes de incorporar, sin reapertura automática. Correcciones históricas tienen alcance separado; elegibilidad futura no aprueba generación de compromisos ni apertura futura.

CA-DEC67-13 a CA-DEC67-15 están PROPUESTOS para revisión en [la nota DEC-67](decision-dec-67.md), no criterios aprobados. Reprogramación al mismo día, bucles/duplicados, recurrencias y mecanismos de asignación futura siguen pendientes. PRD draft.
