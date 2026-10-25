# DEC-67 — Identificación inicial de coincidencias

**Fecha:** 2026-10-12. **Decisión:** CONFIRMADA por aprobación explícita del PO. **Criterios:** CONFIRMADOS por aprobación explícita posterior del PO. DEC-67 parcialmente resuelta.

Otro compromiso de la misma tarea en la fecha de destino se identifica como posible coincidencia y se muestra su estado antes de decidir. La identidad se refiere a la misma tarea persistente, no a coincidencia por nombre o descripción. Esta definición inicial no autoriza fusionar, reemplazar, reutilizar o modificar el candidato ni crear duplicados silenciosamente.

Se aplica al caso de destino de corrección a REPROGRAMADO ya aprobado en DEC-69. No se extiende por inferencia a reglas particulares de recurrencias o recuperación de hábitos. No se descarta automáticamente un candidato por estar resuelto: se muestra su estado y las opciones permitidas siguen pendientes.

## Criterios — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC67-01 | Al evaluar el destino del caso aprobado, otro compromiso de la misma tarea en esa fecha se identifica como posible coincidencia. | DEC-67, aprobación PO; CA-DEC69-09/12. |
| CA-DEC67-02 | Antes de pedir decisión explícita sobre la coincidencia, se muestra el estado efectivo del compromiso candidato. No se fijan opciones por estado todavía. | DEC-67; CA-DEC69-09. |
| CA-DEC67-03 | Encontrar una coincidencia no fusiona, sustituye, reutiliza o modifica automáticamente el candidato ni crea un duplicado silenciosamente; mantiene el bloqueo de aplicación mientras falte decidir. | DEC-67; CA-DEC69-09/12; RN-26. |

CA-DEC67-01 a CA-DEC67-03 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Pendientes: opciones según estado, varios candidatos, vínculos de continuación correspondiente, reprogramaciones sucesivas, fechas admisibles, prevención general de duplicados y recurrencias. No implementación; PRD draft.

## Coincidencia con candidato PENDIENTE — CONFIRMADO

Para un candidato PENDIENTE, el PO aprueba elegir explícitamente entre vincularlo como continuación sin sumar trabajo automáticamente o cambiar la fecha de destino. No se crea otro compromiso silenciosamente. No se cambia por inferencia la planificación del candidato ni se duplica avance; coordinación con corrección origen/destino conjunta conserva CA-DEC69-11 a CA-DEC69-14.

Esta decisión no define opciones para candidatos ya resueltos ni selección entre varios candidatos. La alternativa de cambiar fecha no aprueba todas las fechas posibles ni reglas de asignación futura; la nueva fecha se evalúa bajo las condiciones ya aprobadas.

## CA-DEC67-04 a CA-DEC67-06 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC67-04 | Ante candidato PENDIENTE de la misma tarea en destino, se ofrecen decisiones explícitas de vincularlo como continuación o cambiar fecha destino, sin elegir por el usuario. | DEC-67, nueva aprobación PO; CA-DEC67-01/02/03. |
| CA-DEC67-05 | Elegir vincular el candidato no crea otro compromiso ni suma automáticamente trabajo, metas o avances al candidato; mantiene la trazabilidad de continuación. No se prescribe recalcular su planificación. | DEC-67; RN-26; CA-DEC69-09/10. |
| CA-DEC67-06 | Elegir cambiar la fecha mantiene pendiente la aplicación hasta definir un destino y evaluar posibles coincidencias en esa fecha; no modifica silenciosamente el candidato anterior. | DEC-67; RN-06; CA-DEC69-11/12. |

CA-DEC67-04 a CA-DEC67-06 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Candidatos resueltos, múltiples candidatos, fechas admisibles, recurrencias y duplicados generales siguen pendientes. PRD draft.

## Candidatos ya resueltos — CONFIRMADO

El PO aprueba mostrar compromisos COMPLETADOS, CANCELADOS o REPROGRAMADOS como antecedentes, sin vincularlos como continuación pendiente ni modificar su resultado dentro de este flujo. Si ese es el candidato para el destino, el usuario debe elegir otro destino. Corregir el antecedente requiere procedimiento separado bajo DEC-69 y sus transiciones aprobadas, no una opción silenciosa del flujo de coincidencias.

La selección de otro destino conserva evaluación previa y no confirma automáticamente fechas admisibles. Caso de varios candidatos con estados mixtos sigue pendiente: no se interpreta que un resuelto prohíba vincular cualquier PENDIENTE concurrente sin una regla específica.

## CA-DEC67-07 a CA-DEC67-09 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC67-07 | Un candidato COMPLETADO, CANCELADO o REPROGRAMADO se presenta con su estado como antecedente; no se ofrece convertirlo en continuación PENDIENTE dentro del flujo. | DEC-67, nueva aprobación PO; CA-DEC67-02; catálogo CA-DEC62-35. |
| CA-DEC67-08 | Ante ese candidato resuelto, se exige elegir otro destino y evaluar sus coincidencias antes de aplicar la operación; el antecedente conserva su resultado. No define varios candidatos mixtos. | DEC-67; CA-DEC67-06; CA-DEC69-12. |
| CA-DEC67-09 | Modificar el antecedente resuelto requiere un procedimiento de corrección separado, justificado/auditado y dentro de las transiciones aprobadas; elegir destino no lo corrige ni reabre silenciosamente. | DEC-67; DEC-69; RN-20; CA-DEC69-01 a CA-DEC69-07. |

CA-DEC67-07 a CA-DEC67-09 fueron aprobados explícitamente e incorporados como CONFIRMADOS al borrador. Varios candidatos/estados mixtos, fechas admisibles y recurrencias siguen pendientes. PRD draft.

## Múltiples candidatos — CONFIRMADO

El PO aprueba mostrar todos los candidatos con su estado y permitir seleccionar explícitamente uno PENDIENTE como continuación. Los candidatos resueltos permanecen antecedentes; si no hay ningún PENDIENTE, se debe cambiar destino. No se elige automáticamente ni se fusionan candidatos. Esto precisa el caso de estados mixtos: un resuelto no impide seleccionar un PENDIENTE distinto.

La decisión aborda candidatos existentes, no aprueba creación general de duplicados ni reglas específicas de recurrencias. Seleccionar uno conserva decisiones explícitas y aplicación conjunta origen/destino aprobada; no altera a los no seleccionados.

## CA-DEC67-10 a CA-DEC67-12 — CONFIRMADOS

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC67-10 | Si hay varios candidatos de la misma tarea y fecha destino, se muestran todos con su estado antes de decidir. | DEC-67, nueva aprobación PO; CA-DEC67-01/02. |
| CA-DEC67-11 | Si existe al menos un candidato PENDIENTE, el usuario puede seleccionar explícitamente uno como continuación; no se elige ni fusiona automáticamente y los demás no se modifican por seleccionarlo. | DEC-67; CA-DEC67-04/05. |
| CA-DEC67-12 | Los candidatos resueltos permanecen antecedentes no elegibles como continuación; si no existe ningún PENDIENTE, se exige cambiar destino. Un resuelto no impide seleccionar otro PENDIENTE. | DEC-67; CA-DEC67-07/08; precisión para estados mixtos. |

CA-DEC67-10 a CA-DEC67-12 fueron aprobados e incorporados como CONFIRMADOS al borrador. Fechas admisibles, recurrencias y prevención general de duplicados siguen pendientes. PRD draft.

## Fechas admisibles en reprogramación ordinaria — CONFIRMADO

**Fecha de aprobación:** 2026-10-12. El PO acepta destino en fecha local actual o posterior, no anterior. Se usa fecha actual según zona válida adoptada para el usuario, conforme DEC-68; no se compara únicamente con la fecha del compromiso original.

No se permite incorporar por reprogramación ordinaria a una jornada destino CERRADA. Si corresponde al mismo día y cumple la reapertura autorizada DEC-61, el usuario debe reabrirla explícitamente con justificación antes de incorporarla; la reprogramación no reabre automáticamente. Destinos futuros no cerrados siguen sujetos a reglas de asignación/incorporación todavía pendientes. La elegibilidad de una fecha futura no aprueba por sí sola crear compromisos ni abrir jornadas de esa fecha.

Esta decisión no define fechas destino de correcciones históricas DEC-69 ni generaliza a recurrencias. Tampoco decide cuándo una reprogramación al mismo día procede sobre el compromiso original o cómo evitar bucles/duplicados; esas condiciones conservan su estado pendiente.

## Criterios adicionales — PROPUESTOS para revisión

| ID | Criterio | Origen |
|---|---|---|
| CA-DEC67-13 | Una reprogramación ordinaria admite como fecha elegible la fecha local actual o una posterior; no permite una anterior a la actual. Las demás condiciones siguen aplicándose. | DEC-67, aprobación PO; RN-06; CA-DEC68-01/02/20. |
| CA-DEC67-14 | No se incorpora un compromiso por reprogramación ordinaria a una jornada CERRADA; para una jornada del mismo día se exige reapertura explícita autorizada y justificada antes de incorporarlo. La operación no reabre silenciosamente. | DEC-67; CA-DEC61-01/02/03/04; FR-3. |
| CA-DEC67-15 | El límite de fechas ordinarias no se aplica por inferencia a correcciones históricas ni aprueba creación de compromisos futuros, apertura futura, recurrencias o resolución de duplicados. Sus reglas específicas permanecen pendientes. | DEC-67; DEC-69; RF-027/RN-06. Restricción de alcance de la especificación. |

CA-DEC67-13 a CA-DEC67-15 esperan aprobación para incorporación como CONFIRMADOS. Reprogramación al mismo día, bucles, destinos futuros, correcciones y prevención general de duplicados siguen pendientes. PRD draft.
