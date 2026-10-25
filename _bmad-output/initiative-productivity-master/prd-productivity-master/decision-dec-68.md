# DEC-68 — Día calendario y zona horaria del navegador

**Fecha:** 2026-10-11. **Decisión:** CONFIRMADA por el PO al aceptar límite calendario con precisión de zona del navegador. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. DEC-68 parcialmente resuelta.

Se usa la zona horaria reportada por el navegador del usuario, en lugar de fijar America/Santiago, para determinar fecha local y cambio de día a las 00:00 locales. La reapertura autorizada por DEC-61 corresponde al mismo día local; después del cambio de fecha no se habilita reabrir la anterior por esa excepción. Se conservan los procedimientos de regularización y corrección auditada, sin extender su alcance por inferencia.

## Cambio explícito de DEC-24/RN-24

La decisión sustituye America/Santiago como zona fija inicial por la zona del navegador. Semana desde lunes permanece confirmada. Las fuentes aprobadas de discovery se mantienen como historial; esta precisión posterior prevalece durante PRD.

Zona del navegador significa configuración horaria reportada por el navegador, generalmente vinculada al dispositivo. No se prescribe geolocalización física ni se presupone que siempre coincida con ubicación real. No se elige mecanismo técnico de lectura/detección.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC68-01 | La fecha local utilizada para identificar el día del usuario se determina usando la zona horaria reportada por su navegador, sin fijarla a America/Santiago. | DEC-68 y precisión posterior de DEC-24/RN-24. |
| CA-DEC68-02 | El día calendario cambia a las 00:00 locales de la zona del navegador. | DEC-68, aprobación PO del límite propuesto. |
| CA-DEC68-03 | La reapertura de DEC-61 solo se habilita si la fecha de jornada coincide con el día local actual; después de medianoche no se habilita por esa regla para la fecha anterior. | DEC-68; CA-DEC61-01; CA-JOR-13/20 como antecedentes históricos. |
| CA-DEC68-04 | Aperturas, cierres, reaperturas y avances conservan sus momentos reales; aplicar la zona del navegador no permite registrar nuevas acciones como si hubieran ocurrido en una fecha histórica. | CA-JOR-24; CA-DEC61-05/08; RN-16. Precisión posterior: cambios de zona conservan fechas históricas sin reinterpretación automática. |

## Pendientes

Cambio de zona del navegador con jornadas ya abiertas; momento de adoptar el cambio; tratamiento de jornadas abiertas al cambiar zona; navegador sin zona válida; preferencia manual futura; trabajo que cruza medianoche y reparto temporal de un avance; coexistencia de jornadas y definición exacta de atribución de ejecución. No se aprueban respuestas automáticamente.

No se fija esquema técnico, geolocalización ni fórmulas estadísticas. CA-DEC68-01 a CA-DEC68-04 fueron aprobados e incorporados como CONFIRMADOS; PRD draft.

## Cambio de zona y conservación histórica — CONFIRMADO

El PO aprueba conservar fechas originales del historial al cambiar la zona horaria del navegador. La nueva zona se usa para determinar el día actual, sin trasladar automáticamente jornadas ni avances anteriores. No se reinterpretan fechas históricas por el cambio. Se mantienen momentos reales de acciones y avances.

El tratamiento de una jornada ya abierta cuando cambia la zona, el momento exacto de adopción y la representación visual de momentos siguen pendientes. Esta aprobación no determina esos casos ni modifica reglas de reapertura.

### CA-DEC68-05 a CA-DEC68-07 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-05 | Cambiar la zona reportada por el navegador no modifica las fechas originales de jornadas ni avances históricos. | DEC-68, nueva aprobación PO; RN-08/RN-16 como antecedentes. |
| CA-DEC68-06 | El cambio de zona no traslada automáticamente compromisos, jornadas o avances históricos a otra fecha. No determina qué hacer con jornadas abiertas durante el cambio. | DEC-68; CA-DEC62-06/09 como antecedentes de conservación. La referencia a compromisos preserva el vínculo histórico con jornada, sin definir asignación futura. |
| CA-DEC68-07 | La nueva zona se usa para determinar el día local actual, manteniendo el historial con sus fechas originales. No fija el instante de adopción del cambio ni su efecto en jornadas abiertas. | DEC-68; CA-DEC68-01/02. |

CA-DEC68-05 a CA-DEC68-07 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. PRD draft; sin implementación.

## Jornadas abiertas durante cambio de zona — CONFIRMADO

El PO aprueba conservar, hasta el cierre, la fecha y la zona con las que se abrió una jornada ya abierta cuando cambia la zona del navegador. La nueva zona determina el día actual para las siguientes jornadas. No se cambia automáticamente la fecha ni la zona de la jornada abierta por ese cambio.

Esta precisión limita la aplicación inmediata de la nueva zona en CA-DEC68-07: sigue siendo referencia del día actual, sin reasignar la jornada abierta. No decide cómo atribuir avances ejecutados durante el cambio ni cómo coordinar jornadas que pudieran coincidir, reabrir posteriormente o cruzar medianoche.

### CA-DEC68-08 a CA-DEC68-10 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-08 | Si cambia la zona del navegador mientras una jornada está ABIERTA, esa jornada conserva hasta su cierre la fecha y zona con las que se abrió. | DEC-68, nueva aprobación PO; CA-DEC68-05/06. |
| CA-DEC68-09 | Cambiar la zona no cierra, reabre ni cambia automáticamente el estado de esa jornada; el cierre conserva las condiciones y confirmación manual previamente aprobadas. | DEC-68; CA-JOR-07/08/18. |
| CA-DEC68-10 | La nueva zona determina el día local actual para las siguientes jornadas, sin reasignar por ello la jornada que ya estaba ABIERTA. | DEC-68; CA-DEC68-01/02/07 y nueva precisión PO. |

CA-DEC68-08 a CA-DEC68-10 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Permanecen pendientes atribución de avances durante el cambio, coincidencias y jornadas simultáneas, reapertura posterior, medianoche y zona no válida. No se define mecanismo técnico. PRD draft.

## Nuevos avances después de cambio de zona — CONFIRMADO

El PO aprueba atribuir los nuevos avances a la fecha real de ejecución según la nueva zona reportada por el navegador, aunque su compromiso pertenezca a una jornada abierta con fecha/zona anteriores. Día de compromiso y día de esfuerzo se distinguen; no se reasigna por ello el compromiso o la jornada. Los avances históricos conservan sus fechas originales y los nuevos sus momentos reales.

Esta precisión resuelve atribución de nuevos avances tras cambio de zona, no el reparto de una ejecución que cruza medianoche ni cómo determinar el momento exacto de adopción o capturar ejecuciones con intervalo. No se aprueba trabajo sin compromiso ni regla estadística adicional.

### CA-DEC68-11 a CA-DEC68-13 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-11 | Después de adoptar la nueva zona del navegador, un nuevo avance se atribuye a su fecha real de ejecución en esa zona, aunque el compromiso pertenezca a una jornada abierta con zona anterior. | DEC-68, confirmación explícita PO; RN-16; RF-017. |
| CA-DEC68-12 | Registrar ese avance no cambia la fecha o zona conservada de la jornada abierta ni la fecha de su compromiso. | DEC-68; CA-DEC68-08/10; CA-DEC62-06. |
| CA-DEC68-13 | El esfuerzo del nuevo avance se atribuye a su fecha real y no se duplica para atribuirlo también al día del compromiso; mantiene el vínculo con el compromiso y la tarea. | DEC-68; RN-16/RN-26; RF-017/RF-019; CA-DEC62-09. |

CA-DEC68-11 a CA-DEC68-13 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Continúan pendientes adopción exacta, intervalos que cruzan medianoche, coincidencias, reapertura posterior y zona inválida. PRD draft.

## Sesión que cruza medianoche — CONFIRMADO

El PO elige atribuir una sesión completa a una sola fecha: su fecha de inicio. Una sesión de 23:40 a 00:20 se atribuye completa a la fecha en que comenzó; no se reparte automáticamente en 20 minutos por día ni se atribuye a la fecha de término por el mero paso de medianoche.

Se conservan los momentos reales de inicio y término. La fecha de atribución del esfuerzo es una convención explícita de sesión, que precisa RN-16 y CA-DEC68-11/13 sin falsificar momentos reales. Se mantienen vínculos con tarea/compromiso y ausencia de doble conteo. Esto no define cambios de zona DURANTE la misma sesión, sesiones sin inicio conocido ni mecanismos de captura.

### CA-DEC68-14 a CA-DEC68-16 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-14 | Una sesión que comienza antes de medianoche y termina después se atribuye completamente a su fecha de inicio, sin dividirla automáticamente entre fechas. | DEC-68, elección explícita del PO; precisión de RN-16/RF-017. |
| CA-DEC68-15 | En el ejemplo 23:40–00:20, los 40 minutos se atribuyen a la fecha de inicio; no se atribuyen 20 minutos al día siguiente ni 40 minutos adicionales a la fecha de término. | DEC-68; RN-26/RF-019; CA-DEC68-13. |
| CA-DEC68-16 | La atribución a la fecha de inicio conserva los momentos reales de inicio y término y los vínculos con tarea/compromiso; no cambia la fecha de jornada por terminar después de medianoche. | DEC-68; CA-DEC68-04/12/13; CA-JOR-24. |

CA-DEC68-14 a CA-DEC68-16 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Pendientes: cambio de zona dentro de sesión, inicio desconocido, registro tardío y captura de intervalos. No se prescribe cronómetro, almacenamiento ni nuevas fórmulas de estadísticas. PRD draft.

## Cambio de zona durante una sesión — CONFIRMADO

El PO aprueba que una sesión iniciada antes de cambiar zona conserve la fecha de inicio calculada con la zona vigente al comenzar. Las sesiones nuevas usan la nueva zona. Se conserva atribución completa a inicio y momentos reales; no se redefine retroactivamente la fecha de la sesión en curso.

Esta precisión contextualiza la regla de nuevos avances en nueva zona: una sesión ya iniciada conserva su referencia temporal de inicio; no se trata como sesión nueva por cambiar zona o guardar después. No se define aquí cómo capturar inicio, adoptar el cambio o tratar inicio desconocido.

### CA-DEC68-17 a CA-DEC68-19 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-17 | Si cambia la zona del navegador durante una sesión, su fecha de atribución sigue siendo la fecha de inicio calculada en la zona vigente al comenzar, aunque termine o se registre después del cambio. | DEC-68, aprobación explícita PO; CA-DEC68-14/16. |
| CA-DEC68-18 | Las sesiones iniciadas después de adoptar la nueva zona calculan su fecha de inicio en esa nueva zona, sin cambiar la fecha de sesiones anteriores. | DEC-68; CA-DEC68-05/11 y nueva precisión PO. |
| CA-DEC68-19 | Cambiar de zona durante una sesión no divide ni duplica su esfuerzo: la sesión completa conserva una única fecha de atribución y sus momentos reales. | DEC-68; RN-26; CA-DEC68-13/14/15/16. |

CA-DEC68-17 a CA-DEC68-19 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Adopción exacta del cambio, inicio desconocido, registro tardío y captura de intervalos permanecen pendientes. Sin implementación; PRD draft.

## Adopción automática de nueva zona — CONFIRMADO

El PO aprueba adoptar automáticamente una zona distinta reportada por el navegador cuando la aplicación detecta el cambio. Desde ese momento se usa para nuevas jornadas y sesiones, sin pedir confirmación adicional de cambio de zona. Las jornadas ya abiertas y sesiones ya iniciadas conservan sus referencias temporales aprobadas en CA-DEC68-08/17; el historial mantiene sus fechas.

No se fija frecuencia o mecanismo técnico de detección. Una zona no válida o no disponible sigue pendiente. Las reglas de creación/asignación futura y coexistencia de jornadas no quedan aprobadas por esta decisión.

### CA-DEC68-20 a CA-DEC68-22 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-20 | Cuando la aplicación detecta una zona distinta válida reportada por el navegador, la adopta para nuevas jornadas y sesiones desde ese momento, sin confirmación adicional del usuario. | DEC-68, nueva aprobación explícita PO; CA-DEC68-01/10/18. |
| CA-DEC68-21 | Adoptar la nueva zona conserva fecha y zona de las jornadas ya abiertas hasta cierre y la fecha de inicio calculada con la zona original de sesiones ya iniciadas. | DEC-68; CA-DEC68-08/17. |
| CA-DEC68-22 | La adopción automática no cambia fechas históricas, no cierra/reabre jornadas ni divide o duplica esfuerzo registrado. | DEC-68; CA-DEC68-05/06/09/19. |

CA-DEC68-20 a CA-DEC68-22 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Sin frecuencia de detección prescrita; zona inválida/ausente, inicio desconocido y captura de intervalos siguen pendientes. PRD draft.

## Zona del navegador inválida o ausente — CONFIRMADO

El PO aprueba conservar la última zona válida conocida cuando el navegador no informa una zona válida. Si no existe una zona válida previa, se solicita al usuario seleccionar una. No se impone America/Santiago ni otra zona fija por defecto. La solicitud no define todavía cómo operan las funciones dependientes de fecha antes de responder, la lista de opciones o la persistencia técnica.

La adopción automática de una zona válida del navegador cuando vuelva a detectarse conserva la regla aprobada CA-DEC68-20; no se presume que la selección de respaldo sea una preferencia permanente que la sustituya.

### CA-DEC68-23 a CA-DEC68-25 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-23 | Si el navegador no informa una zona válida y existe una última zona válida conocida, se conserva esa zona para determinar fecha y día local. | DEC-68, nueva aprobación PO; CA-DEC68-01/02/20. |
| CA-DEC68-24 | Si no hay zona válida del navegador ni una última zona válida conocida, se solicita al usuario seleccionar una zona válida, sin imponer una fija por defecto. | DEC-68, nueva aprobación PO; precisión DEC-24/RN-24. |
| CA-DEC68-25 | Cuando posteriormente se detecta una zona válida distinta del navegador, se aplica la adopción automática ya aprobada, preservando historial y referencias de jornadas/sesiones iniciadas. | DEC-68; CA-DEC68-20/21/22. |

CA-DEC68-23 a CA-DEC68-25 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Quedan pendientes las operaciones antes de seleccionar zona, lista y validación de selección, inicio de sesión desconocido, registro tardío y conflictos temporales. No implementación; PRD draft.

## Operaciones cuando no hay zona válida — CONFIRMADO

El PO aprueba permitir consulta de información existente cuando no hay ninguna zona válida disponible, pero exigir seleccionar una antes de realizar operaciones dependientes de fechas, como abrir jornadas o registrar avances. Esto se aplica cuando no existe tampoco última zona válida conocida; no bloquea por ausencia del navegador si el respaldo aprobado proporciona una zona válida.

No se completa por inferencia la clasificación de todas las operaciones ni se habilitan acciones previamente restringidas. Consultar información existente no requiere asumir otra zona por defecto. No se define presentación de horas, mensajes concretos ni tecnología.

### CA-DEC68-26 a CA-DEC68-28 — CONFIRMADOS

| ID | Criterio verificable | Origen |
|---|---|---|
| CA-DEC68-26 | Sin zona válida del navegador ni última zona válida conocida, el usuario puede consultar información existente sin que se le imponga una zona fija por defecto. | DEC-68, nueva aprobación PO; CA-DEC68-23/24. |
| CA-DEC68-27 | En esa situación, abrir jornadas o registrar avances requiere seleccionar previamente una zona válida; intentar esas operaciones no las aplica usando una zona supuesta. | DEC-68; CA-DEC68-24; RN-01/RN-16 como antecedentes. |
| CA-DEC68-28 | Después de seleccionar una zona válida, pueden realizarse las operaciones dependientes de fecha bajo sus demás condiciones ya aprobadas; la selección por sí sola no abre una jornada ni registra avances. | DEC-68; CA-DEC60-02/04; CA-JOR-03/04. |

CA-DEC68-26 a CA-DEC68-28 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Lista completa de operaciones dependientes de fecha y presentación temporal sin zona siguen pendientes. PRD draft.
