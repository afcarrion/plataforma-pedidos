---
description: Revisión del sábado. Detecta qué cambió en la semana y llama a los revisores que correspondan.
argument-hint: "[semana opcional, por ejemplo 05]"
---

Haz la revisión semanal del proyecto integrador.

1. **Semana:** usa `$ARGUMENTS` si viene un número. Si no, toma la entrada más reciente de `LEARNING_LOG.md`. Busca esa semana en `docs/plan/semanas.md` y resume en 2 líneas qué se pedía el viernes y el sábado.
2. **Qué cambió:** si el repositorio usa git, revisa los cambios desde el último reporte de `docs/reviews/` (o de los últimos 7 días). Si no hay git, lista los archivos modificados en los últimos 7 días, sin contar `docs/reviews/`.
3. **Elige revisores** según lo que cambió:
   - ADRs, diagramas, documentos de arquitectura o código de dominio → `revisor-arquitectura`
   - Terraform, infraestructura, despliegue, CI/CD, IAM u observabilidad → `revisor-aws`
   - Notebooks, datos, dbt, modelos, LLM, RAG, agentes o evals → `revisor-datos-ia`
   Lanza en paralelo los que apliquen y pásale a cada uno la semana y la lista de archivos que le tocan.
4. **Consolida** en un solo reporte:
   - Resumen de 3 líneas.
   - Hallazgos de prioridad alta de todos los revisores.
   - Cobertura de la semana: lo que pedía `semanas.md` frente a lo que existe en el repositorio.
   - Lista de acciones con casillas `- [ ]`, como máximo 7.
5. **Guarda** el reporte en `docs/reviews/AAAA-MM-DD-semana-NN.md` con la fecha de hoy.
6. **Termina** sugiriendo 2 líneas para la sección "Hallazgos de la revisión" del learning log. No edites el learning log tú.

No corrijas el trabajo del estudiante; los revisores solo señalan.
