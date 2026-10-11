# Product Brief — Aplicación de Productividad Personal

**Versión:** 1.0  
**Fecha:** 2026-10-11  
**Estado:** Borrador consolidado para validación  
**Tipo de proyecto:** Greenfield  
**Metodología:** BMAD

---

## 1. Resumen ejecutivo

Desarrollar una aplicación web de productividad personal que permita transformar objetivos de largo plazo en acciones mensuales, semanales y diarias.

La aplicación combinará planificación, seguimiento cuantitativo, hábitos recurrentes y un sistema estructurado de apertura y cierre de jornadas.

Su característica principal será exigir una resolución explícita de los compromisos diarios antes de cerrar una jornada, incluyendo justificación obligatoria cuando una actividad se cancela o reprograma.

El producto debe conservar los avances parciales, la planificación original y el historial de decisiones, permitiendo evaluar tanto el cumplimiento de actividades como el progreso real hacia los objetivos.

**Propuesta de valor:** planificar con flexibilidad, ejecutar con claridad y evaluar con responsabilidad.

## 2. Problema que buscamos resolver

**[CONFIRMADO — necesidad expresada]**

Las necesidades principales son:

- Tener un punto de entrada único para comenzar cada jornada.
- Visualizar y modificar lo que se debe realizar durante el día.
- Vincular actividades cotidianas con objetivos de mayor alcance.
- Registrar avances diarios, semanales y mensuales.
- Contar con un procedimiento explícito de cierre de jornada.
- Evitar que los compromisos incumplidos desaparezcan o se posterguen sin explicación.
- Revisar los resultados y preparar los siguientes períodos.

**[PROPUESTO — hipótesis de producto]**

Los gestores tradicionales de tareas pueden permitir la acumulación y postergación de pendientes sin exigir una revisión consciente de lo ocurrido.

La hipótesis central es que combinar planificación con cierres y justificaciones estructuradas mejorará la visibilidad del progreso y reducirá las postergaciones sin seguimiento.

Esta hipótesis todavía no está validada con uso real.

## 3. Visión del producto

Crear un espacio de trabajo personal donde cada jornada tenga un propósito, cada actividad pueda relacionarse con un objetivo y cada resultado quede registrado.

El usuario debe poder responder:

1. ¿Qué quiero conseguir?
2. ¿Qué voy a hacer esta semana y hoy para conseguirlo?
3. ¿Qué hice realmente?
4. ¿Cuánto avancé?
5. ¿Qué no pude cumplir y por qué?
6. ¿Qué debería cambiar en la siguiente planificación?

**Resultado esperado:** desarrollar una práctica sostenible de planificación, ejecución, reflexión y mejora continua.

## 4. Usuarios del producto

### Usuario principal

**[CONFIRMADO]**

Una persona que utiliza la aplicación para organizar su productividad personal, establecer objetivos, gestionar actividades y evaluar su cumplimiento.

Caso inicial: uso individual del propietario del producto.

### Usuarios futuros

**[CONFIRMADO]**

La aplicación debe estar preparada para múltiples usuarios, aunque inicialmente solo la utilice una persona.

**[PROPUESTO]**

Cada usuario tendrá datos aislados, preferencias y zona horaria propia. La colaboración entre usuarios no estará disponible en el MVP.

### Contextos de uso

**[PROPUESTO]**

- Profesionales que necesitan organizar trabajo y aprendizaje.
- Personas que mantienen objetivos simultáneos de distintas áreas de vida.
- Usuarios que desean desarrollar hábitos.
- Personas que necesitan analizar sus postergaciones y medir su progreso.

## 5. Estructura de objetivos

**[CONFIRMADO]**

Jerarquía funcional:

Área de vida → Objetivo → Hito → Tarea.

Las tareas podrán existir de manera independiente, sin estar asociadas obligatoriamente a un objetivo.

Ejemplo:

- Área: Desarrollo profesional.
- Objetivo: Mejorar el nivel de inglés.
- Hito: Completar 20 sesiones de conversación.
- Tarea: Practicar conversación durante 45 minutos.
- Registro: 35 minutos realizados.

**[PROPUESTO]**

Cada objetivo podrá tener descripción, fecha objetivo, prioridad, estado y mediciones de resultado.

Los hitos representarán resultados intermedios verificables.

No todos los objetivos necesitarán hitos ni todas las tareas tendrán métricas cuantitativas.

## 6. Alcance funcional del MVP

### Módulo 1 — Identidad y preferencias

**[CONFIRMADO]**
- Un usuario inicialmente.
- Arquitectura preparada para múltiples usuarios.

**[PROPUESTO]**
- Autenticación básica.
- Perfil personal.
- Zona horaria configurable.
- Aislamiento de datos por usuario.

### Módulo 2 — Áreas, objetivos e hitos

**[CONFIRMADO]**
- Organizar objetivos dentro de áreas de vida.
- Descomponer objetivos mediante hitos.
- Relacionar tareas con hitos.
- Permitir tareas independientes.

**[PROPUESTO]**
- Crear, consultar, editar y archivar áreas, objetivos e hitos.
- Definir metas medibles cuando corresponda.
- Visualizar el progreso acumulado.

### Módulo 3 — Planificación mensual y semanal

**[CONFIRMADO]**
- Planificación manual de cada período.
- Compromisos y actividades específicos para semanas y meses.
- Revisión manual de los resultados al finalizar cada período.
- Resumen automático y espacio de reflexión.
- Definición de compromisos para el período siguiente.

**[PROPUESTO]**
- Vistas de calendario y listas.
- Resumen de carga planificada.
- Detección visual de sobrecarga.
- Comparación de planificado contra ejecutado.

### Módulo 4 — Tareas y planificación diaria

**[CONFIRMADO]**
- Crear y editar tareas.
- Asignar actividades a fechas.
- Definir duración estimada opcional.
- Abrir jornadas manualmente.
- Revisar y modificar compromisos mientras la jornada esté abierta.
- Registrar avances durante el día.

**[PROPUESTO]**
- Prioridad opcional.
- Notas asociadas a la ejecución.
- Indicador de tareas pendientes, realizadas y reprogramadas.
- Vista principal denominada "Mi día".

### Módulo 5 — Seguimiento cuantitativo

**[CONFIRMADO]**
- Registrar tareas completadas.
- Medir avances mediante tiempo, cantidad y porcentaje.
- Conservar el progreso parcial al reprogramar una tarea.

**[PROPUESTO]**
- Soportar unidades de medida explícitas.
- Registrar múltiples avances en distintos momentos.
- Separar valor planificado, valor ejecutado y estado de cumplimiento.
- Mantener historial de los avances.

### Módulo 6 — Hábitos y recurrencias

**[CONFIRMADO]**
- Crear hábitos y tareas recurrentes.
- Configurar ejecuciones diarias o en determinados días.
- Permitir justificar incumplimientos.
- Permitir recuperar sesiones en otras fechas.

**[PROPUESTO]**
- Generar registros individuales por fecha de ejecución.
- Permitir pausar una recurrencia conservando su historial.
- Evitar que una reprogramación modifique automáticamente toda la serie.
- Medir adherencia y continuidad de los hábitos.

### Módulo 7 — Cierre de jornada

**[CONFIRMADO]**
- El cierre diario es manual.
- Todas las actividades del día deben resolverse antes del cierre.
- Una actividad puede completarse, cancelarse o reprogramarse.
- Cancelaciones y reprogramaciones requieren justificación.
- La justificación debe contener una categoría y una explicación textual obligatoria.
- Una reprogramación requiere una fecha de destino.
- Los avances parciales se conservan.
- Las jornadas anteriores pendientes deben regularizarse individualmente, conservando sus fechas originales.

**[PROPUESTO]**
- Mostrar una revisión de tareas antes de confirmar el cierre.
- Permitir registrar una reflexión diaria opcional.
- Evitar modificaciones silenciosas en jornadas cerradas.
- Registrar los cambios posteriores con trazabilidad.
- Ejecutar la validación y confirmación del cierre de forma transaccional.

### Módulo 8 — Revisión semanal y mensual

**[CONFIRMADO]**
- Revisión manual.
- Resumen automático.
- Registro de reflexiones.
- Definición del próximo período.

**[PROPUESTO]**
- Indicadores de cumplimiento y avance.
- Comparación entre compromisos y resultados.
- Resumen de causas de incumplimiento.
- Identificación de objetivos que requieren atención.

### Módulo 9 — Estadísticas

**[CONFIRMADO]**
- Seguimiento diario, semanal y mensual.
- Medición mediante tareas y magnitudes cuantitativas.

**[PROPUESTO]**
- Cumplimiento de compromisos.
- Tiempo planificado y registrado.
- Adherencia a hábitos.
- Reprogramaciones y cancelaciones.
- Avance por objetivos e hitos.
- Consistencia de cierres.
- Evolución histórica.

## 7. Reglas de negocio

### RN-01 — Apertura manual

**[CONFIRMADO]** La jornada debe abrirse manualmente.

### RN-02 — Edición durante la jornada

**[CONFIRMADO]** Las actividades planificadas pueden editarse mientras la jornada permanezca abierta.

### RN-03 — Cierre obligatorio del proceso

**[CONFIRMADO]** Una jornada no puede considerarse cerrada si contiene actividades sin resolver.

### RN-04 — Resolución de compromisos

**[CONFIRMADO]** Cada actividad pendiente debe resolverse mediante cumplimiento, cancelación o reprogramación.

### RN-05 — Justificación

**[CONFIRMADO]** Cancelar o reprogramar requiere seleccionar una categoría y escribir una explicación obligatoria.

### RN-06 — Fecha de reprogramación

**[CONFIRMADO]** Una reprogramación requiere definir una nueva fecha de ejecución.

### RN-07 — Progreso acumulado

**[CONFIRMADO]** Los avances parciales deben conservarse cuando una tarea se reprograma.

### RN-08 — Regularización histórica

**[CONFIRMADO]** Las jornadas antiguas pendientes deben poder revisarse y regularizarse individualmente, conservando sus fechas.

### RN-09 — Hábitos incumplidos

**[CONFIRMADO]** El usuario puede justificar el incumplimiento de un hábito o recuperar su ejecución en otra fecha.

### RN-10 — Cierre periódico

**[CONFIRMADO]** Las revisiones semanales y mensuales son manuales e incorporan resumen automático, reflexión y planificación futura.

### RN-11 — Historial

**[PROPUESTO]** Una reprogramación no debe eliminar la ejecución originalmente prevista ni alterar retroactivamente el registro de cumplimiento del día de origen.

### RN-12 — Integridad

**[PROPUESTO]** Las operaciones de cierre y reprogramación deben protegerse contra actualizaciones parciales, registros duplicados y conflictos concurrentes.

### RN-13 — Autorización

**[PROPUESTO]** Todos los recursos personales deberán quedar asociados a un usuario y sujetos a autorización de acceso.

### RN-14 — Recurrencias

**[PROPUESTO]** Cada ejecución de una actividad recurrente tendrá su propio estado e historial. Reprogramar una ejecución no debe alterar las siguientes ocurrencias de la serie.

## 8. Flujos principales del usuario

### Flujo A — Inicio del día

1. Ingresar a la aplicación.
2. Visualizar compromisos, hábitos y tareas pendientes.
3. Revisar la planificación.
4. Abrir manualmente la jornada.
5. Agregar, modificar o priorizar actividades.
6. Comenzar la ejecución.

### Flujo B — Trabajo diario

1. Seleccionar actividad.
2. Registrar avances o notas.
3. Consultar el progreso.
4. Completar actividades o mantenerlas pendientes.
5. Continuar con los siguientes compromisos.

### Flujo C — Cierre diario

1. Solicitar cierre.
2. Revisar actividades pendientes.
3. Completar las que correspondan.
4. Justificar cancelaciones o reprogramaciones.
5. Definir las fechas de destino.
6. Verificar que no existan actividades sin resolver.
7. Registrar reflexión opcional.
8. Confirmar cierre.
9. Guardar resumen e historial.

### Flujo D — Regularización

1. Detectar jornadas anteriores sin cerrar.
2. Mostrar sus fechas y compromisos.
3. Abrir el proceso de regularización para cada fecha.
4. Registrar resultados y justificaciones.
5. Confirmar cierres individuales.
6. Mantener los datos asociados al período correspondiente.

### Flujo E — Revisión semanal y mensual

1. Seleccionar período.
2. Revisar el resumen automático.
3. Consultar cumplimiento y avances por objetivo.
4. Identificar incumplimientos y causas.
5. Registrar reflexiones.
6. Definir compromisos siguientes.
7. Confirmar el cierre del período.

## 9. Métricas del producto

**[PROPUESTO]**

| Indicador | Definición inicial |
|---|---|
| Cumplimiento diario | Ejecuciones completadas / ejecuciones comprometidas |
| Cumplimiento semanal | Ejecuciones completadas / comprometidas durante la semana |
| Cumplimiento mensual | Ejecuciones completadas / comprometidas durante el mes |
| Tiempo realizado | Suma del tiempo de ejecución registrado |
| Adherencia a hábitos | Sesiones cumplidas / sesiones previstas |
| Reprogramaciones | Cantidad de ejecuciones reprogramadas |
| Cancelaciones | Cantidad de ejecuciones canceladas |
| Consistencia | Jornadas cerradas / jornadas esperadas |
| Avance de objetivos | Valor ejecutado respecto de la meta definida |

Se deberán conservar las métricas de tiempo independientemente del estado de cumplimiento.

Las estadísticas deben evitar contar una reprogramación como actividad completada.

**[PENDIENTE]** Definir el denominador exacto en tareas añadidas o retiradas durante el día, objetivos sin métricas y ejecuciones trasladadas entre períodos.

## 10. Criterios de éxito del MVP

Los siguientes criterios son propuestas para validar el primer producto, no metas previamente aprobadas.

### Éxito funcional

- Es posible crear al menos un objetivo y descomponerlo en hitos y tareas.
- Es posible planificar actividades para un día, una semana y un mes.
- Es posible abrir una jornada y registrar actividades y progresos.
- No puede cerrarse una jornada con compromisos sin resolver.
- No puede reprogramarse o cancelarse una actividad sin justificación válida.
- Las reprogramaciones conservan el progreso previo.
- Es posible mantener hábitos recurrentes y registrar sus ejecuciones.
- Es posible regularizar jornadas anteriores.
- Es posible realizar revisiones semanales y mensuales.
- El dashboard distingue avances, cumplimientos e incumplimientos.

### Éxito de uso

**[PROPUESTO — evaluar después de un período de prueba]**

- Completar al menos 80% de los cierres esperados durante cuatro semanas.
- Registrar al menos una revisión semanal por semana de uso.
- Poder cerrar una jornada sencilla en menos de cinco minutos, sin contar el tiempo dedicado a reflexiones extensas.
- Consultar el progreso hacia un objetivo sin reconstruir manualmente información de días anteriores.

No se propone como criterio de éxito alcanzar un porcentaje elevado de tareas completadas: el propósito del MVP es registrar resultados fielmente, no incentivar métricas artificialmente positivas.

## 11. Fuera del alcance del MVP

**[PROPUESTO]**

- Colaboración y asignación de tareas entre usuarios.
- Equipos, organizaciones y roles empresariales.
- Sincronización con Google Calendar u Outlook.
- Integraciones con Notion, Jira o Asana.
- Planificación automática mediante inteligencia artificial.
- Asistente conversacional integrado.
- Aplicaciones nativas para Android e iOS.
- Notificaciones push complejas.
- Facturación o suscripciones.
- Gamificación avanzada.
- Reportes exportables complejos.
- Múltiples sistemas de permisos organizacionales.

## 12. Restricciones técnicas

**[CONFIRMADO]**

- Frontend: Vue 3.
- Backend: Ruby on Rails.
- Base de datos: PostgreSQL.
- Desarrollo con BMAD.
- Codex como agente de implementación.
- VS Code como entorno de trabajo.

**[PROPUESTO]**

- TypeScript y Vite en frontend.
- Rails API-only.
- Pinia para estado de frontend cuando sea necesario.
- REST/JSON como interfaz.
- RSpec para pruebas de backend.
- Vitest para pruebas de frontend.
- Playwright para pruebas E2E.
- Docker Compose para desarrollo.
- Arquitectura monolítica modular en el backend.
- Evitar infraestructura adicional innecesaria durante el MVP.

Estas propuestas técnicas deberán validarse en la fase de arquitectura.

## 13. Riesgos y mitigaciones

| Riesgo | Impacto | Mitigación propuesta |
|---|---|---|
| Exceso de funcionalidades | Retraso del MVP | Implementar por historias pequeñas y verticales |
| Cierre diario demasiado exigente | Abandono de uso | Diseñar un cierre rápido con justificaciones claras |
| Reprogramaciones repetidas | Pérdida de confianza en las métricas | Mantener historial original e indicadores específicos |
| Recurrencias complejas | Errores y duplicados | Separar reglas recurrentes de ejecuciones |
| Métricas ambiguas | Resultados incorrectos | Documentar fórmulas y casos límite en el PRD |
| Ediciones retroactivas | Pérdida de trazabilidad | Mantener historial auditable |
| Sobrecarga de actividades | Frustración | Mostrar capacidad estimada y facilitar la planificación |
| Crecimiento a multiusuario | Problemas de seguridad | Diseñar autorización y aislamiento desde el inicio |

## 14. Decisiones pendientes para el PRD

**[PENDIENTE]**

1. ¿Se permitirá registrar tareas completadas antes de abrir formalmente una jornada?
2. ¿Se permitirá cerrar una jornada correspondiente al día actual antes de terminar el día?
3. ¿Cómo se tratarán los días sin actividades y los días de descanso?
4. ¿Una jornada cerrada podrá reabrirse o solamente corregirse mediante eventos auditados?
5. ¿Qué categorías de justificación estarán disponibles inicialmente?
6. ¿Cómo se computará el cumplimiento cuando una tarea se agregue después de abrir una jornada?
7. ¿Las metas de tiempo y cantidad se interpretarán como objetivos de ejecución o resultados que requieren confirmación manual?
8. ¿Cómo se manejarán reprogramaciones consecutivas y tareas recurrentes coincidentes?
9. ¿Qué sucede con compromisos semanales y mensuales cuando aún existen jornadas sin cerrar?
10. ¿Qué autenticación mínima se implementará para el primer usuario?

Estas decisiones no bloquean la elaboración del Product Brief, pero deben resolverse antes de implementar las funcionalidades afectadas.

## 15. Principios de diseño

**[PROPUESTO]**

- Simplicidad primero: el usuario debe poder comenzar su jornada sin navegar por varias pantallas.
- Historial confiable: no borrar los incumplimientos mediante una reprogramación.
- Flexibilidad responsable: permitir cambios, pero registrar sus motivos.
- Progreso visible: diferenciar tiempo invertido, actividades realizadas y objetivos alcanzados.
- Diseño escalable: preparado para varios usuarios sin introducir complejidad empresarial prematura.
- Rendición de cuentas sin castigo: explicar los incumplimientos para aprender y mejorar la planificación.

## 16. Próximo entregable

Validar este Product Brief mediante BMAD.

Después de su aprobación:

1. Elaborar el PRD.
2. Resolver reglas y casos límite.
3. Diseñar la experiencia de usuario.
4. Validar la arquitectura.
5. Crear épicas e historias.
6. Iniciar implementación incremental con Codex.

**Estado final del documento:** listo para revisión mediante BMAD; todavía no constituye autorización para implementar.