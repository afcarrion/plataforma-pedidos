---
description: Comité de evaluación para demos y finales. Reúne a los tres revisores, califica con la rúbrica del semestre y da un veredicto.
argument-hint: "<versión: v0.1, v0.2, v1.0, v2.0...>"
---

Convoca al comité de evaluación para la versión `$ARGUMENTS`.

1. **Contexto:**
   - Identifica el semestre por la versión: v0.x y v1.0 → SEM 1; v1.x y v2.0 → SEM 2; v2.x y v3.0 → SEM 3; v3.1-final → Capstone.
   - Lee el proyecto de ese semestre en `docs/plan/proyectos.md` (requisitos, hitos y rúbrica) y las semanas correspondientes en `docs/plan/semanas.md`.
   - Si no viene versión, pregunta cuál evaluar y detente.
2. **Tipo de evaluación:**
   - **Demo (v0.x, v1.1 a v1.3, v2.1 a v2.3):** evalúa el avance esperado hasta esa semana, no el proyecto completo. Califica cada criterio de la rúbrica según lo que ya debería existir.
   - **Entrega final (v1.0, v2.0, v3.0, v3.1-final):** evalúa contra todos los requisitos y la rúbrica completa.
3. **Lanza en paralelo** a los tres revisores: `revisor-arquitectura`, `revisor-aws` y `revisor-datos-ia`. A cada uno indícale la versión, el semestre, el tipo de evaluación y que se enfoque en su especialidad. En SEM 1 el revisor de datos e IA solo revisa lo que haya de datos; si no hay nada, que lo diga en una línea.
4. **Deliberación del comité:** con los resultados de los tres:
   - Marca cada requisito del proyecto como cumplido, parcial o faltante, citando la evidencia (archivo).
   - Califica cada criterio de la rúbrica con sus puntos, justificando cada número en una línea.
   - Suma el total. **Veredicto:** Aprobado (75 o más), Aprobado con observaciones (65 a 74), No aprobado (menos de 65). En una demo, el veredicto es sobre si el avance va en ritmo para aprobar la entrega final.
   - Si los revisores se contradicen, señálalo y explica cuál criterio pesa más para el rol de Arquitecto de Software Cloud con profundidad en IA.
5. **Preguntas de defensa:** escribe 5 preguntas difíciles que un comité técnico real haría sobre este trabajo, centradas en trade-offs.
6. **Guarda** el acta en `docs/reviews/AAAA-MM-DD-comite-$ARGUMENTS.md` con: veredicto, tabla de rúbrica, requisitos, hallazgos principales, preguntas de defensa y acciones con casillas `- [ ]`.
7. Al final, recuerda que en las entregas finales de semestre conviene mostrar el trabajo también a una persona real.

No corrijas el trabajo; el comité evalúa y señala.
