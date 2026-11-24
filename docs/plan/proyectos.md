# Proyectos integradores, requisitos y rúbricas

Cada proyecto se aprueba con **75 de 100 puntos**. Los revisores y el comité califican con estas rúbricas.

---

## SEM 1 · Plataforma de Pedidos v1.0: diseñada y desplegada en AWS

**Entrega:** semana 14 · **Materias:** ARQ-501 + CLD-511

Diseñas la plataforma de pedidos (Pedidos, Inventario, Catálogo, Pagos simulados y Notificaciones) y la despliegas en AWS. El documento de arquitectura y el sistema deben contar la misma historia.

### Requisitos
- [ ] Visión, actores y top 7 de características de arquitectura
- [ ] Diagramas C4 de niveles 1 a 3 y context map de DDD
- [ ] Al menos 10 ADRs con opciones, decisión y consecuencias
- [ ] Servicios en ECS Fargate y Lambda, en una VPC multi-AZ
- [ ] RDS para Pedidos y DynamoDB para Inventario, con estrategia de datos documentada
- [ ] Eventos por EventBridge y SQS con outbox, consumidores idempotentes y DLQ
- [ ] Saga Crear pedido coreografiada y orquestada, con compensaciones
- [ ] Resiliencia y caché medidas con k6
- [ ] Trazas OpenTelemetry, 2 SLOs y 3 alarmas
- [ ] Threat model STRIDE, secretos en Secrets Manager e IAM de privilegio mínimo
- [ ] Pipeline CI/CD con fitness functions

### Entregables
- Etiqueta v1.0 en Git
- Documento de arquitectura (arc42 o Markdown, 15 a 25 páginas)
- Demo grabada de 5 minutos
- Runbook inicial

### Hitos
- Semana 4: Demo v0.1
- Semana 7: Parcial
- Semana 8: Demo v0.2
- Semana 12: Demo v0.3
- Semana 14: Final y entrega v1.0

### Rúbrica

| Criterio | Puntos |
|---|---|
| Trade-offs explícitos y justificados | 25 |
| Coherencia entre documento, código y nube | 25 |
| Funcionamiento en AWS de punta a punta | 20 |
| Operación: observabilidad y seguridad | 15 |
| Claridad del documento | 15 |
| **Total** | **100** |

---

## SEM 2 · Plataforma v2.0: datos, analítica y operación profesional

**Entrega:** semana 29 · **Materias:** DAT-521 + CLD-512

La plataforma queda 100% en Terraform y sus datos fluyen a un data lake. Sobre esos datos construyes análisis, modelos y un dashboard que un negocio usaría.

### Requisitos
- [ ] Toda la infraestructura en Terraform con módulos, estado remoto y plan en pull request
- [ ] Data lake en S3 (raw y curated) con Glue Catalog y Athena
- [ ] Eventos en streaming hacia el lake con Kinesis Firehose
- [ ] Pipeline orquestado, idempotente y con pruebas de calidad
- [ ] Modelo dimensional en dbt documentado
- [ ] Informe de A/B test con rigor estadístico
- [ ] Modelo de cancelación validado y segmentación de clientes
- [ ] Baseline de pronóstico de demanda
- [ ] Dashboard en Streamlit desplegado en AWS
- [ ] Despliegue blue/green con rollback automático
- [ ] Certificación AWS SAA presentada y reporte FinOps

### Entregables
- Etiqueta v2.0 en Git
- Informe ejecutivo de 2 páginas
- Video: destruir y recrear la plataforma
- Runbook actualizado

### Hitos
- Semana 18: Demo v1.1
- Semana 22: Parcial y certificación AWS
- Semana 23: Demo v1.2
- Semana 26: Demo v1.3
- Semana 29: Final y entrega v2.0

### Rúbrica

| Criterio | Puntos |
|---|---|
| Reproducibilidad de la infraestructura | 20 |
| Calidad del pipeline de datos | 20 |
| Rigor estadístico y calidad de los modelos | 25 |
| Operación y costos | 15 |
| Comunicación de hallazgos | 20 |
| **Total** | **100** |

---

## SEM 3 · Plataforma v3.0: IA en producción

**Entrega:** semana 43 · **Materias:** IA-531 + ARQ-532

La plataforma incorpora tres capacidades de IA operables, medidas y seguras, con el mismo nivel de ingeniería que el resto del sistema.

### Requisitos
- [ ] Predicción de demanda versionada en MLflow, desplegada, con monitoreo de drift y reentrenamiento automático
- [ ] Asistente de soporte con RAG, búsqueda híbrida y citas
- [ ] Agente con herramientas expuestas por un servidor MCP y confirmación humana en acciones sensibles
- [ ] Suite de evals con al menos 30 casos que bloquea cambios en CI
- [ ] Red teaming documentado y guardrails activos
- [ ] Observabilidad de LLM: trazas, tokens y costo por solicitud
- [ ] Comparación entre modelo abierto local y modelo por API
- [ ] Model cards y ADRs de IA

### Entregables
- Etiqueta v3.0 en Git
- Reporte de evaluación (calidad, latencia, costo, seguridad)
- Documento de arquitectura de IA
- Demo grabada de 5 minutos

### Hitos
- Semana 34: Demo v2.1
- Semana 36: Parcial
- Semana 38: Demo v2.2
- Semana 42: Demo v2.3
- Semana 43: Final y entrega v3.0

### Rúbrica

| Criterio | Puntos |
|---|---|
| Funcionamiento de punta a punta | 20 |
| Evaluación y calidad medida | 25 |
| Seguridad y guardrails | 15 |
| Operación MLOps y LLMOps | 25 |
| Diseño y documentación | 15 |
| **Total** | **100** |

---

## CAPSTONE · Defensa final de la plataforma

**Entrega:** semana 46 · **Materias:** CAP-540

Presentas la plataforma completa: arquitectura, nube, datos e IA. El objetivo es demostrar criterio, no solo funcionalidades.

### Requisitos
- [ ] Documento de arquitectura v2 que integre los 3 semestres
- [ ] Game day: falla inyectada y recuperación con el runbook
- [ ] Repositorio ordenado con README principal
- [ ] Retrospectiva de las 46 semanas y plan del siguiente año

### Entregables
- Demo grabada de 10 minutos
- Artículo técnico publicado
- Presentación de 12 a 15 diapositivas
- Etiqueta v3.1-final

### Hitos
- Semana 46: Defensa final

### Rúbrica

| Criterio | Puntos |
|---|---|
| Coherencia de la arquitectura integrada | 30 |
| Calidad de la demo y del sistema | 25 |
| Capacidad de explicar trade-offs | 25 |
| Comunicación pública | 20 |
| **Total** | **100** |
