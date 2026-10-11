# Línea base de requisitos — Productivity_Master

**Fecha:** 2026-10-11 · **Estado documental:** consolidado para revisión, no autorización de implementación.

## Convenciones

Requisitos funcionales RF y no funcionales RNF tienen identificadores únicos que no se renumeran al cambiar estado. CONFIRMADO, PROPUESTO y PENDIENTE se interpretan según [decision-log.md](decision-log.md). Los requisitos confirmados describen capacidades aprobadas; sus dependencias abiertas no autorizan inventar detalles. Una referencia a RN confirmada dentro de un requisito propuesto no aprueba el resto del requisito.

Esta línea base es descubrimiento consolidado, no PRD. Las preguntas sin respuesta viven en DEC-60 a DEC-75. Cada requisito tiene estado, dependencias y trazabilidad. «—» significa que no corresponde una regla adicional, no que falte justificación.

## Catálogo por módulo

### M1 — Identidad y preferencias

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-001"></a> RF-001 | CONFIRMADO | Uso individual inicial, preparado para múltiples usuarios. | — | [DEC-30](decision-log.md#dec-30) | [RNF-001](requirements-baseline.md#rnf-001), [RNF-004](requirements-baseline.md#rnf-004) |
| <a id="rf-002"></a> RF-002 | CONFIRMADO | Zona horaria inicial America/Santiago y semana desde lunes; contemplar personalización futura sin fijar entrega. | [RN-24](business-rules.md#rn-24) | [DEC-24](decision-log.md#dec-24) | [DEC-72](decision-log.md#dec-72) |
| <a id="rf-003"></a> RF-003 | PROPUESTO | Autenticación básica, perfil, preferencias y zona horaria por usuario. | [RN-13](business-rules.md#rn-13) | [DEC-38](decision-log.md#dec-38) | [DEC-70](decision-log.md#dec-70), [DEC-72](decision-log.md#dec-72) |

### M2 — Áreas, objetivos e hitos

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-004"></a> RF-004 | CONFIRMADO | Organizar áreas, objetivos, hitos y tareas; permitir tareas independientes. | — | [DEC-31](decision-log.md#dec-31) | [RF-010](requirements-baseline.md#rf-010) |
| <a id="rf-005"></a> RF-005 | PROPUESTO | Crear, consultar, editar y archivar áreas, objetivos e hitos; descripción, fecha objetivo, prioridad, estado y metas medibles. | [RN-29](business-rules.md#rn-29) | [DEC-37](decision-log.md#dec-37) | [DEC-71](decision-log.md#dec-71), [DEC-74](decision-log.md#dec-74) |
| <a id="rf-006"></a> RF-006 | PROPUESTO | Hitos como resultados intermedios verificables; objetivos sin hitos y tareas sin métricas; visualizar progreso acumulado. | [RN-17](business-rules.md#rn-17) | [DEC-37](decision-log.md#dec-37) | [DEC-63](decision-log.md#dec-63), [DEC-74](decision-log.md#dec-74) |
| <a id="rf-007"></a> RF-007 | CONFIRMADO | Impedir archivar objetivo con tareas activas antes de resolverlas o reasignarlas. | [RN-29](business-rules.md#rn-29) | [DEC-29](decision-log.md#dec-29) | [DEC-62](decision-log.md#dec-62) |

### M3 — Planificación mensual y semanal

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-008"></a> RF-008 | CONFIRMADO | Planificar manualmente semanas y meses con compromisos propios. | [RN-10](business-rules.md#rn-10), [RN-24](business-rules.md#rn-24) | [DEC-32](decision-log.md#dec-32) | [RF-029](requirements-baseline.md#rf-029), [DEC-73](decision-log.md#dec-73) |
| <a id="rf-009"></a> RF-009 | PROPUESTO | Calendarios/listas, carga planificada, detección de sobrecarga y comparación planificado/ejecutado. | — | [DEC-39](decision-log.md#dec-39) | [RF-008](requirements-baseline.md#rf-008), [DEC-63](decision-log.md#dec-63) |

### M4 — Tareas y planificación diaria

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-010"></a> RF-010 | CONFIRMADO | Crear y editar tareas, asignar fechas y duración estimada opcional. | [RN-02](business-rules.md#rn-02), [RN-18](business-rules.md#rn-18) | [DEC-36](decision-log.md#dec-36) | [RF-004](requirements-baseline.md#rf-004), [DEC-62](decision-log.md#dec-62) |
| <a id="rf-011"></a> RF-011 | CONFIRMADO | Planificar diariamente, abrir manualmente la jornada y revisar/modificar compromisos mientras esté abierta. | [RN-01](business-rules.md#rn-01), [RN-02](business-rules.md#rn-02) | [DEC-01](decision-log.md#dec-01), [DEC-02](decision-log.md#dec-02), [DEC-32](decision-log.md#dec-32) | [RF-010](requirements-baseline.md#rf-010), [DEC-60](decision-log.md#dec-60) |
| <a id="rf-012"></a> RF-012 | CONFIRMADO | Conservar compromiso original y registrar cambios al editar. | [RN-18](business-rules.md#rn-18) | [DEC-18](decision-log.md#dec-18) | [RF-010](requirements-baseline.md#rf-010) |
| <a id="rf-013"></a> RF-013 | CONFIRMADO | Retirar una tarea exige justificación y conserva compromiso en historial y cálculo de cumplimiento. | [RN-19](business-rules.md#rn-19), [RN-25](business-rules.md#rn-25) | [DEC-19](decision-log.md#dec-19), [DEC-25](decision-log.md#dec-25) | [DEC-62](decision-log.md#dec-62), [DEC-63](decision-log.md#dec-63), [DEC-65](decision-log.md#dec-65) |
| <a id="rf-014"></a> RF-014 | PROPUESTO | Prioridad opcional, notas, indicadores de pendientes/realizadas/reprogramadas y vista Mi día. | — | [DEC-40](decision-log.md#dec-40) | [RF-011](requirements-baseline.md#rf-011), [DEC-62](decision-log.md#dec-62) |
| <a id="rf-015"></a> RF-015 | CONFIRMADO | Declarar descanso sin perjudicar cumplimiento; resolver o trasladar justificadamente compromisos antes de confirmarlo. | [RN-23](business-rules.md#rn-23) | [DEC-23](decision-log.md#dec-23) | [RF-025](requirements-baseline.md#rf-025), [DEC-63](decision-log.md#dec-63), [DEC-64](decision-log.md#dec-64) |

### M5 — Seguimiento cuantitativo

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-016"></a> RF-016 | CONFIRMADO | Registrar avances de tiempo, cantidad y porcentaje y tareas completadas. | [RN-15](business-rules.md#rn-15), [RN-17](business-rules.md#rn-17) | [DEC-33](decision-log.md#dec-33) | [RF-010](requirements-baseline.md#rf-010), [DEC-74](decision-log.md#dec-74) |
| <a id="rf-017"></a> RF-017 | CONFIRMADO | Conservar avances parciales al reprogramar; atribuir avances a su fecha real. | [RN-07](business-rules.md#rn-07), [RN-16](business-rules.md#rn-16) | [DEC-07](decision-log.md#dec-07), [DEC-16](decision-log.md#dec-16) | [RF-027](requirements-baseline.md#rf-027), [DEC-68](decision-log.md#dec-68) |
| <a id="rf-018"></a> RF-018 | CONFIRMADO | Completar exclusivamente mediante confirmación explícita incluso al alcanzar 100 %. | [RN-15](business-rules.md#rn-15) | [DEC-15](decision-log.md#dec-15) | [RF-016](requirements-baseline.md#rf-016) |
| <a id="rf-019"></a> RF-019 | CONFIRMADO | Separar cumplimiento, esfuerzo y avance hacia objetivos; no duplicar ejecuciones o progreso. | [RN-17](business-rules.md#rn-17), [RN-26](business-rules.md#rn-26) | [DEC-17](decision-log.md#dec-17), [DEC-26](decision-log.md#dec-26) | [DEC-63](decision-log.md#dec-63), [DEC-74](decision-log.md#dec-74) |
| <a id="rf-020"></a> RF-020 | PROPUESTO | Unidades explícitas, múltiples registros, valores planificado/ejecutado e historial de avances. | [RN-16](business-rules.md#rn-16), [RN-17](business-rules.md#rn-17) | [DEC-41](decision-log.md#dec-41) | [RF-016](requirements-baseline.md#rf-016) |

### M6 — Hábitos y recurrencias

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-021"></a> RF-021 | CONFIRMADO | Crear hábitos y tareas recurrentes diarias o en días seleccionados. | — | [DEC-34](decision-log.md#dec-34) | [RF-010](requirements-baseline.md#rf-010), [DEC-62](decision-log.md#dec-62) |
| <a id="rf-022"></a> RF-022 | CONFIRMADO | Justificar incumplimientos o recuperar sesiones en otra fecha; recuperación separada sin borrar incumplimiento original. | [RN-09](business-rules.md#rn-09), [RN-21](business-rules.md#rn-21) | [DEC-09](decision-log.md#dec-09), [DEC-21](decision-log.md#dec-21) | [RF-025](requirements-baseline.md#rf-025), [DEC-66](decision-log.md#dec-66), [DEC-67](decision-log.md#dec-67) |
| <a id="rf-023"></a> RF-023 | CONFIRMADO | Cambiar frecuencia solo afecta sesiones futuras. | [RN-22](business-rules.md#rn-22) | [DEC-22](decision-log.md#dec-22) | [RF-021](requirements-baseline.md#rf-021), [DEC-75](decision-log.md#dec-75) |
| <a id="rf-024"></a> RF-024 | PROPUESTO | Ejecuciones individuales con estado/historial; reprogramación sin alterar serie; pausa con historial; adherencia y continuidad. | [RN-14](business-rules.md#rn-14) | [DEC-14](decision-log.md#dec-14), [DEC-42](decision-log.md#dec-42) | [RF-021](requirements-baseline.md#rf-021), [DEC-67](decision-log.md#dec-67) |

### M7 — Cierre de jornada

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-025"></a> RF-025 | CONFIRMADO | Cierre diario manual únicamente con todos los compromisos resueltos: completar, cancelar o reprogramar. | [RN-03](business-rules.md#rn-03), [RN-04](business-rules.md#rn-04) | [DEC-03](decision-log.md#dec-03), [DEC-04](decision-log.md#dec-04) | [RF-018](requirements-baseline.md#rf-018), [RF-026](requirements-baseline.md#rf-026), [RF-027](requirements-baseline.md#rf-027) |
| <a id="rf-026"></a> RF-026 | CONFIRMADO | Cancelar o reprogramar exige categoría y explicación textual obligatorias. | [RN-05](business-rules.md#rn-05) | [DEC-05](decision-log.md#dec-05) | [DEC-65](decision-log.md#dec-65) |
| <a id="rf-027"></a> RF-027 | CONFIRMADO | Reprogramar exige fecha destino, conserva progreso y compromiso original sin marcarlo completado. | [RN-06](business-rules.md#rn-06), [RN-07](business-rules.md#rn-07), [RN-11](business-rules.md#rn-11) | [DEC-06](decision-log.md#dec-06), [DEC-07](decision-log.md#dec-07), [DEC-11](decision-log.md#dec-11) | [RF-017](requirements-baseline.md#rf-017), [RF-026](requirements-baseline.md#rf-026), [DEC-67](decision-log.md#dec-67) |
| <a id="rf-028"></a> RF-028 | CONFIRMADO | Regularizar individualmente jornadas antiguas conservando sus fechas originales; corregir jornadas cerradas con justificación y auditoría, sin reapertura. | [RN-08](business-rules.md#rn-08), [RN-20](business-rules.md#rn-20) | [DEC-08](decision-log.md#dec-08), [DEC-20](decision-log.md#dec-20) | [DEC-69](decision-log.md#dec-69) |
| <a id="rf-030"></a> RF-030 | PROPUESTO | Revisión de tareas previa al cierre y reflexión diaria opcional. | — | [DEC-40](decision-log.md#dec-40) | [RF-025](requirements-baseline.md#rf-025) |

### M8 — Revisión semanal y mensual

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-029"></a> RF-029 | CONFIRMADO | Revisar/cerrar manualmente semanas y meses con resumen automático, reflexiones y próximos compromisos. | [RN-10](business-rules.md#rn-10) | [DEC-10](decision-log.md#dec-10) | [RF-008](requirements-baseline.md#rf-008), [RF-034](requirements-baseline.md#rf-034), [DEC-73](decision-log.md#dec-73) |
| <a id="rf-031"></a> RF-031 | CONFIRMADO | Bloquear cierre periódico si hay jornadas comprometidas pendientes de regularización. | [RN-27](business-rules.md#rn-27) | [DEC-27](decision-log.md#dec-27) | [RF-028](requirements-baseline.md#rf-028), [RF-029](requirements-baseline.md#rf-029), [DEC-62](decision-log.md#dec-62), [DEC-73](decision-log.md#dec-73) |
| <a id="rf-032"></a> RF-032 | CONFIRMADO | Conservar revisiones originales e historial al corregir; actualizar estadísticas actuales. | [RN-28](business-rules.md#rn-28) | [DEC-28](decision-log.md#dec-28) | [RF-028](requirements-baseline.md#rf-028), [RF-034](requirements-baseline.md#rf-034), [DEC-69](decision-log.md#dec-69) |
| <a id="rf-033"></a> RF-033 | PROPUESTO | Comparar compromisos/resultados, causas de incumplimiento y objetivos que requieren atención. | [RN-17](business-rules.md#rn-17) | [DEC-43](decision-log.md#dec-43) | [RF-029](requirements-baseline.md#rf-029), [DEC-63](decision-log.md#dec-63) |

### M9 — Estadísticas

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rf-034"></a> RF-034 | CONFIRMADO | Seguimiento diario, semanal y mensual mediante tareas y magnitudes; distinguir cumplimiento, esfuerzo y avance. | [RN-16](business-rules.md#rn-16), [RN-17](business-rules.md#rn-17), [RN-26](business-rules.md#rn-26) | [DEC-33](decision-log.md#dec-33), [DEC-17](decision-log.md#dec-17), [DEC-26](decision-log.md#dec-26) | [RF-016](requirements-baseline.md#rf-016), [RF-019](requirements-baseline.md#rf-019), [DEC-63](decision-log.md#dec-63) |
| <a id="rf-035"></a> RF-035 | CONFIRMADO | Contar todos los compromisos asumidos, incluidos retiros; admitir incorporación formal; cancelados/reprogramados no son completados. | [RN-19](business-rules.md#rn-19), [RN-25](business-rules.md#rn-25) | [DEC-19](decision-log.md#dec-19), [DEC-25](decision-log.md#dec-25) | [DEC-62](decision-log.md#dec-62), [DEC-63](decision-log.md#dec-63) |
| <a id="rf-036"></a> RF-036 | PROPUESTO | Indicadores de cumplimiento, tiempo planificado/registrado, adherencia, reprogramaciones/cancelaciones, objetivos/hitos, consistencia y evolución histórica. | [RN-17](business-rules.md#rn-17) | [DEC-43](decision-log.md#dec-43) | [RF-034](requirements-baseline.md#rf-034), [DEC-63](decision-log.md#dec-63), [DEC-74](decision-log.md#dec-74) |

### Transversal — Requisitos no funcionales

| ID | Estado | Requisito | Reglas | Decisiones | Dependencias principales |
|---|---|---|---|---|---|
| <a id="rnf-001"></a> RNF-001 | CONFIRMADO | Frontend Vue 3 + TypeScript, backend Ruby on Rails API-only, PostgreSQL; VS Code + Codex y BMAD. | — | [DEC-35](decision-log.md#dec-35) | — |
| <a id="rnf-002"></a> RNF-002 | CONFIRMADO | Historial confiable: conservar originales, cambios y correcciones justificadas/auditadas; evitar doble contabilización. | [RN-11](business-rules.md#rn-11), [RN-18](business-rules.md#rn-18), [RN-19](business-rules.md#rn-19), [RN-20](business-rules.md#rn-20), [RN-21](business-rules.md#rn-21), [RN-26](business-rules.md#rn-26), [RN-28](business-rules.md#rn-28) | [DEC-11](decision-log.md#dec-11), [DEC-18](decision-log.md#dec-18), [DEC-19](decision-log.md#dec-19), [DEC-20](decision-log.md#dec-20), [DEC-21](decision-log.md#dec-21), [DEC-26](decision-log.md#dec-26), [DEC-28](decision-log.md#dec-28) | [DEC-69](decision-log.md#dec-69) |
| <a id="rnf-003"></a> RNF-003 | PROPUESTO | Integridad transaccional y protección contra conflictos concurrentes en cierre/reprogramación. | [RN-12](business-rules.md#rn-12) | [DEC-12](decision-log.md#dec-12) | [RF-025](requirements-baseline.md#rf-025), [RF-027](requirements-baseline.md#rf-027) |
| <a id="rnf-004"></a> RNF-004 | PROPUESTO | Aislamiento de datos y autorización de recursos por usuario. Estrategia concreta pendiente. | [RN-13](business-rules.md#rn-13) | [DEC-13](decision-log.md#dec-13), [DEC-38](decision-log.md#dec-38) | [RF-001](requirements-baseline.md#rf-001), [DEC-70](decision-log.md#dec-70) |
| <a id="rnf-005"></a> RNF-005 | PROPUESTO | Vite, Pinia, REST/JSON, RSpec, Vitest, Playwright, Docker Compose, backend monolítico modular e infraestructura mínima. | — | [DEC-44](decision-log.md#dec-44) | [RNF-001](requirements-baseline.md#rnf-001); validación futura en arquitectura |
| <a id="rnf-006"></a> RNF-006 | PROPUESTO | Simplicidad, flexibilidad responsable y rendición de cuentas sin castigo; cierre sencillo menor a cinco minutos como criterio propuesto. | — | [DEC-47](decision-log.md#dec-47), [DEC-49](decision-log.md#dec-49) | [DEC-65](decision-log.md#dec-65) |

## Dependencias entre capacidades

Identidad y calendario soportan las tres escalas temporales. La organización de objetivos y tareas soporta planificación y seguimiento. El cierre depende de resolución explícita, justificación, fecha destino e historial; no de haber alcanzado una métrica. Recurrencias dependen de distinguir sesiones y recuperación. Revisión periódica depende de regularización y resumen estadístico. Estadísticas dependen de fechas reales, conservación histórica, no duplicación y fórmulas aún pendientes.

Autorización, transacciones y herramientas técnicas siguen propuestas: la preparación multiusuario y la confiabilidad confirmadas no seleccionan por sí mismas una implementación. No se inventan objetivos numéricos de disponibilidad, rendimiento, accesibilidad, respaldo o retención; si se necesitan, deberán elicitarse y aprobarse antes del trabajo afectado.

## Validación funcional propuesta

Se conserva §10 del original como criterios PROPUESTOS ([DEC-47](decision-log.md#dec-47)): crear objetivo/hitos/tareas; planificar día/semana/mes; abrir jornada y registrar actividades/progreso; impedir cierre con compromisos sin resolver; impedir cancelación/reprogramación sin justificación válida; conservar progreso; gestionar hábitos/ejecuciones; regularizar jornadas; revisar semanas/meses; dashboard que distinga avance, cumplimiento e incumplimiento. El dashboard y sus detalles siguen PROPUESTOS, aunque la distinción conceptual está CONFIRMADA.

## Matriz de trazabilidad por capacidad

| Capacidad / brief | Requisitos | Reglas | Decisiones principales |
|---|---|---|---|
| Usuarios y calendario | [RF-001](requirements-baseline.md#rf-001) a [RF-003](requirements-baseline.md#rf-003); [RNF-001](requirements-baseline.md#rnf-001), [RNF-004](requirements-baseline.md#rnf-004) | [RN-13](business-rules.md#rn-13), [RN-24](business-rules.md#rn-24) | [DEC-24](decision-log.md#dec-24), [DEC-30](decision-log.md#dec-30), [DEC-35](decision-log.md#dec-35), [DEC-38](decision-log.md#dec-38), [DEC-70](decision-log.md#dec-70), [DEC-72](decision-log.md#dec-72) |
| Organización y archivo | [RF-004](requirements-baseline.md#rf-004) a [RF-007](requirements-baseline.md#rf-007) | [RN-29](business-rules.md#rn-29) | [DEC-29](decision-log.md#dec-29), [DEC-31](decision-log.md#dec-31), [DEC-37](decision-log.md#dec-37), [DEC-71](decision-log.md#dec-71) |
| Planificación periódica | [RF-008](requirements-baseline.md#rf-008), [RF-009](requirements-baseline.md#rf-009) | [RN-10](business-rules.md#rn-10), [RN-24](business-rules.md#rn-24) | [DEC-32](decision-log.md#dec-32), [DEC-39](decision-log.md#dec-39), [DEC-73](decision-log.md#dec-73) |
| Jornada, edición y descanso | [RF-010](requirements-baseline.md#rf-010) a [RF-015](requirements-baseline.md#rf-015) | [RN-01](business-rules.md#rn-01), [RN-02](business-rules.md#rn-02), [RN-18](business-rules.md#rn-18), [RN-19](business-rules.md#rn-19), [RN-23](business-rules.md#rn-23), [RN-25](business-rules.md#rn-25) | [DEC-01](decision-log.md#dec-01), [DEC-02](decision-log.md#dec-02), [DEC-18](decision-log.md#dec-18), [DEC-19](decision-log.md#dec-19), [DEC-23](decision-log.md#dec-23), [DEC-25](decision-log.md#dec-25), [DEC-36](decision-log.md#dec-36), [DEC-40](decision-log.md#dec-40) |
| Seguimiento | [RF-016](requirements-baseline.md#rf-016) a [RF-020](requirements-baseline.md#rf-020) | [RN-07](business-rules.md#rn-07), [RN-15](business-rules.md#rn-15), [RN-16](business-rules.md#rn-16), [RN-17](business-rules.md#rn-17), [RN-26](business-rules.md#rn-26) | [DEC-07](decision-log.md#dec-07), [DEC-15](decision-log.md#dec-15), [DEC-16](decision-log.md#dec-16), [DEC-17](decision-log.md#dec-17), [DEC-26](decision-log.md#dec-26), [DEC-33](decision-log.md#dec-33), [DEC-41](decision-log.md#dec-41) |
| Hábitos | [RF-021](requirements-baseline.md#rf-021) a [RF-024](requirements-baseline.md#rf-024) | [RN-09](business-rules.md#rn-09), [RN-14](business-rules.md#rn-14), [RN-21](business-rules.md#rn-21), [RN-22](business-rules.md#rn-22) | [DEC-09](decision-log.md#dec-09), [DEC-14](decision-log.md#dec-14), [DEC-21](decision-log.md#dec-21), [DEC-22](decision-log.md#dec-22), [DEC-34](decision-log.md#dec-34), [DEC-42](decision-log.md#dec-42) |
| Cierre y regularización | [RF-025](requirements-baseline.md#rf-025) a [RF-028](requirements-baseline.md#rf-028); [RF-030](requirements-baseline.md#rf-030); [RNF-002](requirements-baseline.md#rnf-002), [RNF-003](requirements-baseline.md#rnf-003) | [RN-03](business-rules.md#rn-03) a [RN-08](business-rules.md#rn-08), [RN-11](business-rules.md#rn-11), [RN-12](business-rules.md#rn-12), [RN-20](business-rules.md#rn-20) | [DEC-03](decision-log.md#dec-03) a [DEC-08](decision-log.md#dec-08), [DEC-11](decision-log.md#dec-11), [DEC-12](decision-log.md#dec-12), [DEC-20](decision-log.md#dec-20), [DEC-40](decision-log.md#dec-40) |
| Revisiones y estadísticas | [RF-029](requirements-baseline.md#rf-029), [RF-031](requirements-baseline.md#rf-031) a [RF-036](requirements-baseline.md#rf-036) | [RN-10](business-rules.md#rn-10), [RN-16](business-rules.md#rn-16), [RN-17](business-rules.md#rn-17), [RN-19](business-rules.md#rn-19), [RN-25](business-rules.md#rn-25) a [RN-28](business-rules.md#rn-28) | [DEC-10](decision-log.md#dec-10), [DEC-16](decision-log.md#dec-16), [DEC-17](decision-log.md#dec-17), [DEC-19](decision-log.md#dec-19), [DEC-25](decision-log.md#dec-25) a [DEC-28](decision-log.md#dec-28), [DEC-33](decision-log.md#dec-33), [DEC-43](decision-log.md#dec-43) |
| Propuestas transversales | [RNF-005](requirements-baseline.md#rnf-005), [RNF-006](requirements-baseline.md#rnf-006) | [RN-12](business-rules.md#rn-12), [RN-13](business-rules.md#rn-13) | [DEC-44](decision-log.md#dec-44), [DEC-47](decision-log.md#dec-47), [DEC-49](decision-log.md#dec-49) |
| Hipótesis, exclusiones y entregas | Brief: hipótesis, fuera de alcance, MVP | No agregan reglas confirmadas | [DEC-45](decision-log.md#dec-45) a [DEC-48](decision-log.md#dec-48) |

Los rangos son resúmenes; las filas individuales del catálogo ofrecen los enlaces exactos. Las decisiones normativas [DEC-01](decision-log.md#dec-01) a [DEC-44](decision-log.md#dec-44) y [DEC-50](decision-log.md#dec-50) incluyen a continuación referencias inversas; hipótesis/exclusiones/criterios/secuencia/principios [DEC-45](decision-log.md#dec-45) a [DEC-49](decision-log.md#dec-49) se conservan en el brief y registro, sin inventar requisitos aprobados.

## Índice inverso de decisiones a requisitos

| Decisión | Requisitos que la citan |
|---|---|
| [DEC-01](decision-log.md#dec-01) | [RF-011](requirements-baseline.md#rf-011) |
| [DEC-02](decision-log.md#dec-02) | [RF-011](requirements-baseline.md#rf-011) |
| [DEC-03](decision-log.md#dec-03) | [RF-025](requirements-baseline.md#rf-025) |
| [DEC-04](decision-log.md#dec-04) | [RF-025](requirements-baseline.md#rf-025) |
| [DEC-05](decision-log.md#dec-05) | [RF-026](requirements-baseline.md#rf-026) |
| [DEC-06](decision-log.md#dec-06) | [RF-027](requirements-baseline.md#rf-027) |
| [DEC-07](decision-log.md#dec-07) | [RF-017](requirements-baseline.md#rf-017), [RF-027](requirements-baseline.md#rf-027) |
| [DEC-08](decision-log.md#dec-08) | [RF-028](requirements-baseline.md#rf-028) |
| [DEC-09](decision-log.md#dec-09) | [RF-022](requirements-baseline.md#rf-022) |
| [DEC-10](decision-log.md#dec-10) | [RF-029](requirements-baseline.md#rf-029) |
| [DEC-11](decision-log.md#dec-11) | [RF-027](requirements-baseline.md#rf-027), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-12](decision-log.md#dec-12) | [RNF-003](requirements-baseline.md#rnf-003) |
| [DEC-13](decision-log.md#dec-13) | [RNF-004](requirements-baseline.md#rnf-004) |
| [DEC-14](decision-log.md#dec-14) | [RF-024](requirements-baseline.md#rf-024) |
| [DEC-15](decision-log.md#dec-15) | [RF-018](requirements-baseline.md#rf-018) |
| [DEC-16](decision-log.md#dec-16) | [RF-017](requirements-baseline.md#rf-017) |
| [DEC-17](decision-log.md#dec-17) | [RF-019](requirements-baseline.md#rf-019), [RF-034](requirements-baseline.md#rf-034) |
| [DEC-18](decision-log.md#dec-18) | [RF-012](requirements-baseline.md#rf-012), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-19](decision-log.md#dec-19) | [RF-013](requirements-baseline.md#rf-013), [RF-035](requirements-baseline.md#rf-035), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-20](decision-log.md#dec-20) | [RF-028](requirements-baseline.md#rf-028), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-21](decision-log.md#dec-21) | [RF-022](requirements-baseline.md#rf-022), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-22](decision-log.md#dec-22) | [RF-023](requirements-baseline.md#rf-023) |
| [DEC-23](decision-log.md#dec-23) | [RF-015](requirements-baseline.md#rf-015) |
| [DEC-24](decision-log.md#dec-24) | [RF-002](requirements-baseline.md#rf-002) |
| [DEC-25](decision-log.md#dec-25) | [RF-013](requirements-baseline.md#rf-013), [RF-035](requirements-baseline.md#rf-035) |
| [DEC-26](decision-log.md#dec-26) | [RF-019](requirements-baseline.md#rf-019), [RF-034](requirements-baseline.md#rf-034), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-27](decision-log.md#dec-27) | [RF-031](requirements-baseline.md#rf-031) |
| [DEC-28](decision-log.md#dec-28) | [RF-032](requirements-baseline.md#rf-032), [RNF-002](requirements-baseline.md#rnf-002) |
| [DEC-29](decision-log.md#dec-29) | [RF-007](requirements-baseline.md#rf-007) |
| [DEC-30](decision-log.md#dec-30) | [RF-001](requirements-baseline.md#rf-001) |
| [DEC-31](decision-log.md#dec-31) | [RF-004](requirements-baseline.md#rf-004) |
| [DEC-32](decision-log.md#dec-32) | [RF-008](requirements-baseline.md#rf-008), [RF-011](requirements-baseline.md#rf-011) |
| [DEC-33](decision-log.md#dec-33) | [RF-016](requirements-baseline.md#rf-016), [RF-034](requirements-baseline.md#rf-034) |
| [DEC-34](decision-log.md#dec-34) | [RF-021](requirements-baseline.md#rf-021) |
| [DEC-35](decision-log.md#dec-35) | [RNF-001](requirements-baseline.md#rnf-001) |
| [DEC-36](decision-log.md#dec-36) | [RF-010](requirements-baseline.md#rf-010) |
| [DEC-37](decision-log.md#dec-37) | [RF-005](requirements-baseline.md#rf-005), [RF-006](requirements-baseline.md#rf-006) |
| [DEC-38](decision-log.md#dec-38) | [RF-003](requirements-baseline.md#rf-003), [RNF-004](requirements-baseline.md#rnf-004) |
| [DEC-39](decision-log.md#dec-39) | [RF-009](requirements-baseline.md#rf-009) |
| [DEC-40](decision-log.md#dec-40) | [RF-014](requirements-baseline.md#rf-014), [RF-030](requirements-baseline.md#rf-030) |
| [DEC-41](decision-log.md#dec-41) | [RF-020](requirements-baseline.md#rf-020) |
| [DEC-42](decision-log.md#dec-42) | [RF-024](requirements-baseline.md#rf-024) |
| [DEC-43](decision-log.md#dec-43) | [RF-033](requirements-baseline.md#rf-033), [RF-036](requirements-baseline.md#rf-036) |
| [DEC-44](decision-log.md#dec-44) | [RNF-005](requirements-baseline.md#rnf-005) |
| [DEC-50](decision-log.md#dec-50) | Necesidades transversales realizadas por RF-004, RF-008, RF-010, RF-011, RF-016, RF-025, RF-029 y RF-034. |

## Cobertura de la fuente original

| Sección original | Conservación en documentos nuevos |
|---|---|
| §1 Resumen | Brief; [DEC-17](decision-log.md#dec-17), [RNF-002](requirements-baseline.md#rnf-002). |
| §2 Problema | Brief; [DEC-46](decision-log.md#dec-46) (hipótesis), [DEC-50](decision-log.md#dec-50) (necesidades). |
| §3 Visión | Brief: visión, preguntas que orientan el uso y propuesta de valor. |
| §4 Usuarios | Brief; [RF-001](requirements-baseline.md#rf-001) a [RF-003](requirements-baseline.md#rf-003); [DEC-30](decision-log.md#dec-30), [DEC-38](decision-log.md#dec-38), [DEC-46](decision-log.md#dec-46). |
| §5 Jerarquía y ejemplo | [RF-004](requirements-baseline.md#rf-004) a [RF-007](requirements-baseline.md#rf-007); [DEC-31](decision-log.md#dec-31), [DEC-37](decision-log.md#dec-37); reglas: ejemplo 11. |
| §6 Módulos | Catálogo [RF-001](requirements-baseline.md#rf-001) a [RF-036](requirements-baseline.md#rf-036), requisitos RNF y decisiones [DEC-30](decision-log.md#dec-30) a [DEC-44](decision-log.md#dec-44). |
| §7 RN originales | Catálogo [RN-01](business-rules.md#rn-01) a [RN-14](business-rules.md#rn-14); registro explícito de diferencias. |
| §8 Flujos A–E | business-rules.md: flujos preservados, con estados de propuestas. |
| §9 Indicadores | business-rules.md: definiciones preliminares; [DEC-43](decision-log.md#dec-43), [DEC-63](decision-log.md#dec-63). |
| §10 Éxito | Brief; validación funcional anterior; [DEC-47](decision-log.md#dec-47). |
| §11 Exclusiones | Brief; [DEC-45](decision-log.md#dec-45), todas PROPUESTAS. |
| §12 Restricciones | [RNF-001](requirements-baseline.md#rnf-001), [RNF-005](requirements-baseline.md#rnf-005); [DEC-35](decision-log.md#dec-35), [DEC-44](decision-log.md#dec-44); promoción explícita de TypeScript y API-only; observación previa de JavaScript registrada. |
| §13 Riesgos | Brief; [DEC-49](decision-log.md#dec-49); [RNF-002](requirements-baseline.md#rnf-002) a [RNF-004](requirements-baseline.md#rnf-004). |
| §14 Preguntas | [DEC-60](decision-log.md#dec-60) a [DEC-75](decision-log.md#dec-75); preguntas parcialmente resueltas diferenciadas en decision-log.md. |
| §15 Principios | [DEC-49](decision-log.md#dec-49); [RNF-006](requirements-baseline.md#rnf-006); no promover principios a decisiones funcionales adicionales. |
| §16 Próximo entregable | decision-log.md: ruta futura como contexto, sin iniciar trabajo. |

## Resultado de revisión de consistencia

- Los nueve módulos y las 16 secciones del original están cubiertos; las confirmaciones posteriores del PO tienen registros y trazabilidad.
- [RN-01](business-rules.md#rn-01) a [RN-29](business-rules.md#rn-29) existen una vez en el catálogo. [RN-12](business-rules.md#rn-12), [RN-13](business-rules.md#rn-13) y [RN-14](business-rules.md#rn-14) siguen PROPUESTAS; los aspectos confirmados se separan y enlazan.
- No se duplican IDs. M3 define planificación y M8 revisión; M5 registro de avances y M9 estadísticas. Las referencias compartidas son trazabilidad, no requisitos adicionales.
- No se detecta una contradicción resuelta mediante una regla inventada. La tensión descanso/compromisos está abierta en [DEC-63](decision-log.md#dec-63); retiro/resolución en [DEC-62](decision-log.md#dec-62); hábitos/resolución en [DEC-66](decision-log.md#dec-66).
- Las fórmulas originales se preservan como propuestas preliminares. Estados técnicos, mecanismos de autorización y agregaciones no se fijan.
- El archivo fuente conserva su contenido de trabajo capturado al crear los documentos; no se escribió en él. Su estado respecto de HEAD se informa mediante Git al finalizar.
- La integridad de IDs/enlaces y el hash del original se verifican al finalizar. Esta revisión documental no demuestra eficacia de la hipótesis ni viabilidad temporal del MVP.
