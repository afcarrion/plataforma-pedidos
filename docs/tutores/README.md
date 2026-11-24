# Equipo docente

Hay dos tipos de agentes:

| Tipo | Dónde vive | Para qué |
|---|---|---|
| **Tutores** | Proyectos de claude.ai | Estudiar: te explican, te preguntan y te toman exámenes |
| **Revisores** | `.claude/agents/` en este repositorio (Claude Code) | Revisar lo que construiste leyendo tus archivos |

## Tutores: cómo crear cada Proyecto en claude.ai

Repite estos pasos para cada uno de los 4 tutores:

1. Entra a claude.ai y abre **Proyectos → Crear proyecto**.
2. **Nombre:** el del tutor (por ejemplo, "Tutor de Arquitectura").
3. **Instrucciones del proyecto:** copia y pega el contenido completo de su archivo:

| Tutor | Archivo con las instrucciones | Cuándo usarlo |
|---|---|---|
| Tutor de Arquitectura | [tutor-arquitectura.md](tutor-arquitectura.md) | Semestre 1 y materia ARQ-532 del semestre 3 |
| Tutor de Cloud y AWS | [tutor-cloud.md](tutor-cloud.md) | Semestres 1 y 2, preparación SAA |
| Tutor de Datos e IA | [tutor-datos-ia.md](tutor-datos-ia.md) | Semestres 2 y 3 |
| Entrevistador de system design | [entrevistador.md](entrevistador.md) | Parciales, finales y práctica libre |

4. **Conocimiento del proyecto:** sube estos 3 archivos de `docs/plan/`:
   - `plan.md`
   - `semanas.md`
   - `proyectos.md`
5. Opcional: conecta tu repositorio de GitHub al Proyecto cuando lo tengas, para que el tutor vea tus ADRs.

## Cómo empezar una sesión con un tutor

Abre una conversación nueva dentro del Proyecto y escribe, por ejemplo:

> Estoy en la semana 6. Leí replicación y particionamiento en DDIA. Hazme preguntas para ver si lo entendí.

Al terminar, copia las ideas clave a tu `LEARNING_LOG.md`.

## Revisores: cómo usarlos en Claude Code

Abre esta carpeta (`plataforma-pedidos`) en Claude Code y escribe:

| Qué quieres | Qué escribes |
|---|---|
| Revisión del sábado | `/revision-semanal` |
| Comité de una demo o entrega | `/comite-demo v0.1` (o la versión que toque) |
| Un revisor en particular | "Usa el revisor-aws para revisar la carpeta infra" |

Los tres revisores son de solo lectura: señalan problemas, pero no cambian tus archivos. Los reportes se guardan en `docs/reviews/`.

## Mantener el conocimiento al día

Si cambias el plan, vuelve a subir `semanas.md` y `proyectos.md` a los Proyectos de los tutores.
