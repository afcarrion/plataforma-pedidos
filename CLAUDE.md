# Contexto para Claude

Este repositorio es el **proyecto integrador** de un plan de estudio de 46 semanas. Lo construye un desarrollador backend con más de 7 años de experiencia, cuyo objetivo es llegar a **Arquitecto de Software Cloud con profundidad en IA**.

## Dónde está cada cosa

- Plan general, semestres e hitos: `docs/plan/plan.md`
- Detalle de cada semana y actividad: `docs/plan/semanas.md`
- Requisitos y rúbricas de los proyectos integradores: `docs/plan/proyectos.md`
- Semana actual: la entrada más reciente de `LEARNING_LOG.md`
- ADRs: `docs/architecture/decisions/` (formato en `0000-plantilla.md`)
- Reportes de revisión anteriores: `docs/reviews/`

## Cómo ayudar

- **Es un proyecto de aprendizaje.** Ayuda a entender, depurar y destrabar, pero no escribas un entregable completo (un ADR, un módulo de Terraform, un servicio) salvo que se pida explícitamente. Si piden "hazlo", hazlo; si piden ayuda, guía.
- Responde en español.
- Para revisar trabajo usa los subagentes de `.claude/agents/` o los comandos `/revision-semanal` y `/comite-demo`.
- Nunca pongas secretos, llaves ni credenciales en el repositorio.

## Convenciones

- ADRs numerados `NNNN-titulo-en-kebab.md`, con estado: Propuesto, Aceptado, Reemplazado por NNNN.
- Etiquetas de versión: v0.1, v0.2… por demo; v1.0, v2.0, v3.0 por semestre; v3.1-final al cierre.
- Reportes de revisión en `docs/reviews/AAAA-MM-DD-<tipo>.md`.
