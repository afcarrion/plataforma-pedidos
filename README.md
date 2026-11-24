# Plataforma de Pedidos

Proyecto integrador de mi plan de estudio **Ruta Senior** (46 semanas): arquitectura de software, AWS, datos e inteligencia artificial.
El objetivo profesional es llegar a **Arquitecto de Software Cloud con profundidad en IA**.

> La visión, los actores y los casos de uso se completan en la semana 1.

## Visión

_Pendiente (semana 1)._

## Actores

_Pendiente (semana 1)._

## Casos de uso principales

_Pendiente (semana 1)._

## Bounded contexts

Pedidos · Inventario · Catálogo · Pagos (simulados) · Notificaciones

## Estado por versión

| Versión | Semestre | Qué incluye | Estado |
|---|---|---|---|
| v1.0 | SEM 1 · Diseñar y desplegar | Plataforma diseñada y corriendo en AWS | Pendiente |
| v2.0 | SEM 2 · Datos de la plataforma | Terraform, data lake, modelos y dashboard | Pendiente |
| v3.0 | SEM 3 · IA en producción | Predicción de demanda, asistente RAG y agente | Pendiente |
| v3.1-final | Capstone | Defensa final | Pendiente |

## Estructura del repositorio

```
docs/architecture/decisions/   ADRs (registro de decisiones)
docs/architecture/diagrams/    Diagramas C4 como código
docs/plan/                     Plan de estudio, semanas y rúbricas
docs/reviews/                  Reportes de los revisores y del comité
docs/tutores/                  Instrucciones de los tutores (Proyectos de claude.ai)
.claude/agents/                Subagentes revisores de Claude Code
.claude/commands/              Comandos /revision-semanal y /comite-demo
LEARNING_LOG.md                Bitácora semanal
```

## Equipo docente

Ver [docs/tutores/README.md](docs/tutores/README.md).

- **Tutores** (Proyectos de claude.ai): Arquitectura, Cloud y AWS, IA, y un entrevistador de system design.
- **Revisores** (subagentes de Claude Code, solo lectura): `revisor-arquitectura`, `revisor-aws`, `revisor-datos-ia`.
- **Comandos**: `/revision-semanal` cada sábado y `/comite-demo` en semanas de demo y finales.
