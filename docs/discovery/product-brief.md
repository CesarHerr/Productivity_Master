# Product Brief — Productivity_Master

**Fecha:** 2026-10-11 · **Estado documental:** consolidado para revisión, no autorización de implementación.

## Resumen ejecutivo

Aplicación web de productividad personal para transformar objetivos de largo plazo en acciones mensuales, semanales y diarias. Su núcleo confirmado combina planificación manual, seguimiento cuantitativo, hábitos y cierre explícito: cada compromiso diario debe completarse, cancelarse o reprogramarse antes de cerrar. Cancelar y reprogramar requieren categoría y explicación; reprogramar también exige fecha destino.

**Propuesta de valor:** planificar con flexibilidad, ejecutar con claridad y evaluar con responsabilidad. Conservar planificación original, avances parciales e historial permite distinguir cumplimiento, esfuerzo y progreso hacia objetivos.

## Problema, necesidades y visión

**CONFIRMADO — necesidades:** un punto de entrada diario; visualizar y modificar actividades; vincularlas con objetivos; registrar avances diarios, semanales y mensuales; cerrar explícitamente; conservar incumplimientos y revisar resultados para preparar períodos siguientes ([DEC-50](decision-log.md#dec-50)).

**Visión:** una práctica sostenible de planificación, ejecución, reflexión y mejora. El usuario debe saber qué quiere conseguir, qué hará hoy y esta semana, qué hizo, cuánto avanzó, qué incumplió y por qué, y qué cambiará después.

## Usuario principal y evolución

**CONFIRMADO:** uso individual inicial del propietario, preparado para múltiples usuarios. Organización Área de vida → Objetivo → Hito → Tarea, con tareas independientes permitidas. Semana desde lunes y zona horaria inicial `America/Santiago`; se contempla personalización futura, sin fijar alcance o entrega.

**PROPUESTO:** profesionales que organizan trabajo y aprendizaje, personas con objetivos en distintas áreas de vida, hábitos o necesidad de analizar postergaciones. Perfil, aislamiento y preferencias por usuario son propuestas; autenticación y estrategia de autorización están pendientes.

## Capacidades esenciales y alcance del MVP

**CONFIRMADO:**

- Planificación manual diaria, semanal y mensual con compromisos propios en semanas y meses; tareas con duración estimada opcional; edición trazable; apertura/cierre diarios manuales; tiempo, cantidad y porcentaje; cumplimiento por confirmación explícita incluso al 100 %; avances en su fecha real.
- Hábitos diarios o en días seleccionados y recuperación separada del incumplimiento original; descansos sin penalización, resolviendo compromisos antes de declararlos.
- Regularización individual de jornadas antiguas; correcciones justificadas/auditadas sin reapertura; revisiones periódicas con resumen, reflexión y próximos compromisos, bloqueadas por jornadas comprometidas pendientes. Las correcciones actualizan estadísticas, preservando revisiones originales. Archivar objetivos exige resolver o reasignar tareas activas.

**PENDIENTE:** conceptos y estados, fórmulas, identidad/acceso y límites temporales; resolver antes de implementar las capacidades afectadas. Véanse [DEC-60 a DEC-75](decision-log.md#preguntas-abiertas).

**PROPUESTO — entregas incrementales:** (1) ciclo diario con objetivos, seguimiento y trazabilidad; (2) planificación y revisión semanal/mensual; (3) hábitos, recuperación y estadísticas ampliadas. Esta secuencia no elimina capacidades confirmadas del MVP completo ni constituye historias o un plan de implementación ([DEC-48](decision-log.md#dec-48)). Calendarios, detección de sobrecarga, dashboard e indicadores avanzados siguen propuestos.

**Stack confirmado:** Vue 3 + TypeScript, Rails API-only, PostgreSQL, VS Code + Codex y BMAD. Las herramientas adicionales continúan propuestas para evaluación futura, no decididas aquí ([DEC-44](decision-log.md#dec-44)).

## Fuera de alcance — PROPUESTO

Colaboración/asignación entre usuarios; equipos, organizaciones y roles empresariales; integración con Google Calendar, Outlook, Notion, Jira o Asana; planificación por IA y asistente conversacional; apps nativas Android/iOS; push complejo; facturación/suscripciones; gamificación avanzada; reportes exportables complejos y permisos organizacionales múltiples. Estas exclusiones aún requieren aprobación ([DEC-45](decision-log.md#dec-45)).

## Hipótesis y criterios de éxito — PROPUESTO

Los cierres y justificaciones estructurados podrían mejorar la visibilidad del progreso y reducir postergaciones sin seguimiento. **No hay validación con uso real ni evidencia comparativa sobre otros gestores.**

Validación funcional: crear objetivo/hitos/tareas; planificar las tres escalas; abrir y registrar progreso; impedir cierres sin resolver y cancelación/reprogramación sin justificación; conservar avances; usar hábitos, regularización y revisiones; distinguir avances/cumplimientos/incumplimientos en dashboard. Prueba propuesta de cuatro semanas: 80 % de cierres esperados, una revisión semanal por semana, cierre sencillo menor a cinco minutos excluyendo reflexión extensa y consulta de progreso sin reconstrucción manual. No buscar alto porcentaje de completado como éxito del producto. Fórmulas y jornadas esperadas siguen pendientes ([DEC-47](decision-log.md#dec-47)).

## Riesgos principales

Alcance amplio, cierre exigente y abandono; reprogramaciones repetidas; recurrencias y duplicados; métricas ambiguas; correcciones retroactivas; sobrecarga y evolución multiusuario. Mitigaciones propuestas: incrementos, cierre rápido, indicadores de postergación, separación conceptual de recurrencia/ejecución, fórmulas explícitas, capacidad estimada y autorización/aislamiento. La trazabilidad y la ausencia de doble conteo sí están confirmadas.

## Documentos de soporte

[Requisitos y trazabilidad](requirements-baseline.md), [reglas y ejemplos](business-rules.md) y [decisiones, procedencia y preguntas](decision-log.md) conservan el detalle de [la fuente original intacta](../product-brief-v1.md). La consolidación no inicia PRD, arquitectura, épicas, historias ni código.
