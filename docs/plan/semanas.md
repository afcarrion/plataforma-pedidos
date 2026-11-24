# Plan semana a semana

Generado desde la página del plan (ruta-senior.html). Cada semana tiene 4 sesiones de 2 horas: lunes (materia A), miércoles (materia B), viernes (laboratorio integrado) y sábado (proyecto integrador).

---

# SEM 1 · Diseñar y desplegar (semanas 1 a 14)

Cada decisión de arquitectura se implementa en AWS la misma semana. Terminas con la plataforma de pedidos diseñada, documentada y corriendo en la nube.

**Materias:** ARQ-501 Arquitectura de Software Avanzada · CLD-511 Cloud I: Fundamentos de AWS

**Hitos:** S04 Demo v0.1 · S07 Parcial · S08 Demo v0.2 · S12 Demo v0.3 · S14 Final y entrega v1.0

## S01 · Características de arquitectura · Well-Architected

**Objetivo:** Identificar y priorizar las características de un sistema y conocer el marco con el que AWS evalúa una arquitectura.

**Conceptos clave:** Leyes de la arquitectura · Características explícitas e implícitas · Riesgo arquitectónico · 6 pilares de Well-Architected · Responsabilidad compartida

**Autoevaluación:**
1. ¿Por qué se priorizan como máximo 7 características?
2. ¿Qué pilar de Well-Architected cubre cada una de tus características?
3. ¿Por qué no se usa el usuario root en el día a día?

### Lunes · Teoría · ARQ-501 · FoSA: rol del arquitecto y características

Lee los primeros capítulos de Fundamentals of Software Architecture (2.ª edición), enfocado en las leyes de la arquitectura y en cómo extraer características de los requisitos.

**Pasos:**
1. Capítulos 1 y 2: expectativas del arquitecto y pensamiento arquitectónico (45 min).
2. Capítulos 4 y 5: definición e identificación de características (45 min).
3. Capítulo 6: medir y gobernar características (20 min).
4. Anota 5 ideas clave en LEARNING_LOG.md (10 min).

**Terminado cuando:** Puedes explicar en 2 minutos qué es una característica de arquitectura con 3 ejemplos de tu trabajo.

**Recursos:**
  - [O'Reilly: Fundamentals of Software Architecture](https://learning.oreilly.com/search/?q=Fundamentals%20of%20Software%20Architecture)

### Miércoles · Teoría · CLD-511 · Well-Architected y arranque del curso SAA

Lee el marco de buenas prácticas de AWS e inicia el curso de Stephane Maarek, que seguirás todo el semestre.

**Pasos:**
1. Whitepaper: principios generales y los 6 pilares (60 min).
2. Curso: introducción y configuración (20 min).
3. Curso: primera mitad de la sección de IAM (30 min).
4. Resumen de 1 página con una práctica por pilar (10 min).

**Terminado cuando:** Resumen de los 6 pilares listo.

**Recursos:**
  - [Web: AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: cuenta AWS segura y características por pilar

Prepara una cuenta segura con control de costos y relaciona las características de un sistema real con los pilares de AWS.

**Pasos:**
1. MFA en el usuario root; guárdalo fuera de uso.
2. IAM Identity Center con un usuario administrador y AWS CLI configurado con SSO.
3. Alarma en AWS Budgets de 15 USD con avisos al 50% y 80%; activa CloudTrail.
4. Elige un sistema de tu trabajo: lista sus 7 características principales y asigna a cada una el pilar que la cubre.

**Terminado cuando:** Entras sin root, recibes el aviso de prueba del presupuesto y tienes la tabla característica → pilar.

**Recursos:**
  - [Web: Buenas prácticas de IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
  - [Web: AWS Budgets](https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html)
  - [Web: Architecture Katas](https://nealford.com/katas/)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Visión de la Plataforma de Pedidos

Arranca el proyecto integrador que crecerá las 46 semanas: una plataforma de pedidos con Pedidos, Inventario, Catálogo, Pagos simulados y Notificaciones.

**Pasos:**
1. Crea el repositorio plataforma-pedidos.
2. README con visión, actores (cliente, operador, pasarela de pago) y 6 casos de uso.
3. docs/architecture/characteristics.md con el top 7 justificado y el pilar AWS de cada una.
4. LEARNING_LOG.md con la retro de 15 min: qué aprendí, qué me costó, qué aplico en el trabajo.

**Terminado cuando:** Repositorio con README, características y primera entrada del learning log.

**Recursos:**
  - [Web: Cómo escribir un buen README](https://www.makeareadme.com/)

## S02 · Documentar arquitectura · IAM y EC2

**Objetivo:** Comunicar una arquitectura con diagramas y decisiones registradas, y dominar identidad y cómputo básico en AWS.

**Conceptos clave:** Modelo C4 · ADRs · arc42 · Roles y políticas IAM · EC2 y tipos de instancia

**Autoevaluación:**
1. ¿Qué debe tener un ADR para seguir siendo útil en 2 años?
2. ¿Qué diagrama C4 le muestras a un gerente y cuál a un desarrollador nuevo?
3. ¿Diferencia entre un rol y un usuario IAM?

### Lunes · Teoría · ARQ-501 · C4, ADRs y arc42

Aprende a documentar arquitectura sin escribir documentos que nadie lee.

**Pasos:**
1. Capítulo de diagramación de FoSA (30 min).
2. c4model.com: niveles, notación y errores comunes (30 min).
3. Charla de Simon Brown sobre C4 (40 min).
4. Artículo de Michael Nygard sobre ADRs y plantilla MADR (20 min).

**Terminado cuando:** Sabes qué va en cada nivel de C4 y escribes un ADR sin mirar la plantilla.

**Recursos:**
  - [Web: Modelo C4](https://c4model.com/)
  - [Web: ADRs (Michael Nygard)](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
  - [YouTube: Simon Brown Visualising software architecture with the C4 model](https://www.youtube.com/results?search_query=Simon%20Brown%20Visualising%20software%20architecture%20with%20the%20C4%20model)

### Miércoles · Teoría · CLD-511 · Curso SAA: IAM y EC2

Continúa el curso de Maarek.

**Pasos:**
1. Resto de la sección de IAM.
2. Sección de fundamentos de EC2.
3. Quizzes de ambas secciones.

**Terminado cuando:** Quizzes con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: C4 como código y mapa de servicios AWS

Modela la plataforma con Structurizr y decide qué servicio de AWS usará cada contenedor.

**Pasos:**
1. C4 nivel 1 (contexto) y nivel 2 (contenedores) en Structurizr DSL.
2. Para cada contenedor elige un servicio AWS y una alternativa.
3. Estima el costo mensual en AWS Pricing Calculator.
4. Guarda el .dsl y docs/cloud/service-map.md.

**Terminado cuando:** Diagramas versionados y tabla de servicios con costo estimado.

**Recursos:**
  - [Web: Structurizr DSL](https://docs.structurizr.com/dsl)
  - [Web: AWS Pricing Calculator](https://calculator.aws/)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Carpeta de arquitectura y primeros ADRs

Deja la estructura de documentación que alimentarás todo el plan.

**Pasos:**
1. docs/architecture con decisions/ y diagrams/.
2. ADR-001: lenguaje y framework del backend.
3. ADR-002: estilo de arquitectura inicial (provisional).
4. ADR-003: AWS como nube y región principal, con su impacto en costo y latencia.
5. Retro en el learning log.

**Terminado cuando:** 3 ADRs con contexto, opciones, decisión y consecuencias.

**Recursos:**
  - [Web: MADR](https://adr.github.io/madr/)

## S03 · Estilos monolíticos y hexagonal · Redes en AWS

**Objetivo:** Saber cuándo un monolito modular bien hecho supera a los microservicios, y diseñar una red segura en AWS.

**Conceptos clave:** Capas, monolito modular, microkernel · Puertos y adaptadores · Fitness functions · VPC, subnets, NAT · Security Groups y NACLs

**Autoevaluación:**
1. ¿Qué resuelve el monolito modular frente a un monolito en capas?
2. ¿Por qué una subnet privada necesita NAT para salir a internet?
3. ¿Cómo verificas automáticamente que el dominio no depende de la infraestructura?

### Lunes · Teoría · ARQ-501 · FoSA: estilos monolíticos y hexagonal

Estilos monolíticos de FoSA, el artículo original de arquitectura hexagonal y una charla de monolitos modulares.

**Pasos:**
1. FoSA: estilo en capas, monolito modular y microkernel (50 min).
2. Artículo de Alistair Cockburn sobre hexagonal (20 min).
3. Charla de monolitos modulares de Simon Brown o Kamil Grzybek (40 min).
4. Tabla: estilo, fortalezas, debilidades, cuándo usarlo (10 min).

**Terminado cuando:** Tabla comparativa de al menos 4 estilos.

**Recursos:**
  - [O'Reilly: Fundamentals of Software Architecture modular monolith](https://learning.oreilly.com/search/?q=Fundamentals%20of%20Software%20Architecture%20modular%20monolith)
  - [Web: Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture/)
  - [YouTube: modular monolith architecture talk](https://www.youtube.com/results?search_query=modular%20monolith%20architecture%20talk)

### Miércoles · Teoría · CLD-511 · Redes en AWS

Diseño de VPC con AWS Cookbook y la sección de VPC del curso.

**Pasos:**
1. AWS Cookbook: capítulo de redes (40 min).
2. Curso de Maarek: sección de VPC (70 min).
3. Quiz de la sección (10 min).

**Terminado cuando:** Puedes dibujar una VPC de 2 AZ con sus tablas de rutas.

**Recursos:**
  - [O'Reilly: AWS Cookbook networking](https://learning.oreilly.com/search/?q=AWS%20Cookbook%20networking)
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: VPC multi-AZ a mano

Construye la red de la plataforma desde la consola para entender cada pieza. En el semestre 2 la pasarás a Terraform.

**Pasos:**
1. VPC con 2 subnets públicas y 2 privadas en 2 AZ.
2. Internet Gateway, NAT Gateway y tablas de rutas.
3. Security Groups: ALB (80/443 público), servicios (solo desde el ALB), base de datos (solo desde servicios).
4. Lanza una EC2 en la subnet privada y verifica salida a internet por NAT.
5. Borra el NAT Gateway al terminar: cobra por hora.

**Terminado cuando:** La EC2 privada sale a internet y no es accesible desde afuera.

**Recursos:**
  - [Web: Documentación de Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Núcleo de Pedidos en hexagonal

Implementa el dominio de Pedidos con puertos y adaptadores en tu lenguaje habitual.

**Pasos:**
1. Entidades Pedido y LineaPedido con sus invariantes.
2. Caso de uso CrearPedido que depende solo del puerto PedidoRepository.
3. Adaptadores en memoria y PostgreSQL; tests de dominio sin base de datos.
4. Fitness function (ArchUnit, NetArchTest o dependency-cruiser) que falle si el dominio importa infraestructura.
5. ADR-004: monolito modular vs. microservicios con matriz de características.

**Terminado cuando:** Tests verdes, fitness function que falla si rompes la regla y ADR-004 escrito.

**Recursos:**
  - [Web: ArchUnit](https://www.archunit.org/)
  - [Web: NetArchTest](https://github.com/BenMorris/NetArchTest)
  - [Web: dependency-cruiser](https://github.com/sverweij/dependency-cruiser)

## S04 · Domain-Driven Design · Alta disponibilidad · Demo v0.1

**Objetivo:** Partir el sistema por el dominio y ponerlo a correr detrás de un balanceador con autoescalado.

**Conceptos clave:** Subdominios core, supporting y generic · Bounded contexts y context mapping · Agregados y eventos de dominio · ALB, NLB y Auto Scaling · Route 53

**Autoevaluación:**
1. ¿Cuándo pones una Anti-Corruption Layer?
2. ¿Cuándo usas NLB en vez de ALB?
3. ¿Qué señal indica que un agregado es demasiado grande?

### Lunes · Teoría · ARQ-501 · Learning Domain-Driven Design y Event Storming

DDD estratégico y táctico con Vlad Khononov, más la técnica de Event Storming.

**Pasos:**
1. Parte I: subdominios, lenguaje ubicuo y bounded contexts (50 min).
2. Parte II: agregados, value objects y eventos (40 min).
3. Charla introductoria de Event Storming de Alberto Brandolini (30 min).

**Terminado cuando:** Clasificas los 5 dominios de la plataforma en core, supporting o generic.

**Recursos:**
  - [O'Reilly: Learning Domain-Driven Design Khononov](https://learning.oreilly.com/search/?q=Learning%20Domain-Driven%20Design%20Khononov)
  - [YouTube: Event Storming Alberto Brandolini](https://www.youtube.com/results?search_query=Event%20Storming%20Alberto%20Brandolini)

### Miércoles · Teoría · CLD-511 · Curso SAA: ELB, Auto Scaling y Route 53

Secciones de alta disponibilidad del curso.

**Pasos:**
1. Sección de ELB y Auto Scaling Groups.
2. Sección de Route 53 y políticas de enrutamiento.
3. Quizzes.

**Terminado cuando:** Quizzes con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: Pedidos detrás de un ALB con autoescalado

Despliega el núcleo hexagonal de Pedidos en la VPC de la semana pasada.

**Pasos:**
1. Recrea el NAT si lo borraste.
2. Launch template con user-data que instala y arranca el servicio.
3. Auto Scaling Group de 2 instancias en subnets privadas detrás de un ALB público.
4. Termina una instancia y verifica que el ALB sigue respondiendo y el ASG la reemplaza.
5. Destruye todo al terminar.

**Terminado cuando:** El servicio responde durante la caída de una instancia.

**Recursos:**
  - [Web: Tutorial ALB con Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/tutorial-ec2-auto-scaling-load-balancer.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Context map y Demo v0.1

Formaliza los límites del sistema y graba la primera demo.

**Pasos:**
1. Event Storming individual en Excalidraw o Miro: al menos 25 eventos.
2. Context map de Pedidos, Inventario, Catálogo, Pagos y Notificaciones con sus relaciones.
3. Glosario en ubiquitous-language.md.
4. Demo v0.1 (3 min): el diseño y Pedidos corriendo en AWS en el lab del viernes.

**Terminado cuando:** Context map, glosario y video de la demo v0.1.

**Recursos:**
  - [Web: Excalidraw](https://excalidraw.com/)
  - [Web: Context Mapper](https://contextmapper.org/)

## S05 · Microservicios y granularidad · Contenedores en AWS

**Objetivo:** Decidir cuánto partir el sistema con criterios objetivos y correr los servicios en contenedores administrados.

**Conceptos clave:** Desintegradores e integradores · Base de datos por servicio · Consumer-driven contracts · ECS, Fargate y ECR · Task definitions y services

**Autoevaluación:**
1. Nombra 3 integradores que te harían unir dos servicios.
2. ¿Qué riesgos trae compartir base de datos entre servicios?
3. ¿Diferencia entre task definition y service en ECS?

### Lunes · Teoría · ARQ-501 · The Hard Parts: granularidad

Capítulos de descomposición y granularidad de Software Architecture: The Hard Parts, más patrones de microservices.io.

**Pasos:**
1. Descomposición basada en componentes (35 min).
2. Granularidad: desintegradores e integradores (45 min).
3. microservices.io: decompose by subdomain, database per service, API gateway (40 min).

**Terminado cuando:** Lista de desintegradores e integradores con un ejemplo de cada uno.

**Recursos:**
  - [O'Reilly: Software Architecture The Hard Parts](https://learning.oreilly.com/search/?q=Software%20Architecture%20The%20Hard%20Parts)
  - [Web: microservices.io](https://microservices.io/patterns/)

### Miércoles · Teoría · CLD-511 · Curso SAA: contenedores

Sección de contenedores del curso y la guía de AWS para elegir cómputo.

**Pasos:**
1. Sección de ECS, Fargate, ECR y EKS (80 min).
2. Guía de decisión de cómputo de AWS (30 min).
3. Quiz (10 min).

**Terminado cuando:** Quiz con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Elegir cómputo en AWS](https://aws.amazon.com/getting-started/decision-guides/compute-on-aws-how-to-choose/)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: Pedidos e Inventario en ECS Fargate

Separa Inventario como servicio propio y despliega ambos en contenedores.

**Pasos:**
1. Servicio Inventario con su API y su propia base local para desarrollo.
2. Imágenes en ECR.
3. Dos servicios ECS Fargate detrás de un ALB con enrutamiento por ruta (/pedidos, /inventario).
4. Logs en CloudWatch y health checks.
5. Escala a 0 al terminar.

**Terminado cuando:** Ambos servicios responden a través del ALB.

**Recursos:**
  - [Web: ECS con Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started-fargate.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Contratos y ADR de granularidad

Asegura que los servicios evolucionen sin romperse y justifica la granularidad.

**Pasos:**
1. Contrato OpenAPI de cada servicio versionado en el repo.
2. Contract test con Pact: Pedidos (consumidor) e Inventario (proveedor).
3. ADR-005: granularidad de toda la plataforma con tabla de análisis.
4. C4 de contenedores actualizado.

**Terminado cuando:** Contract test verde y ADR-005 escrito.

**Recursos:**
  - [Web: Pact](https://docs.pact.io/)
  - [Web: OpenAPI](https://learn.openapis.org/)

## S06 · Datos distribuidos · Bases de datos administradas

**Objetivo:** Entender las garantías reales de una base distribuida y elegir el almacén de cada servicio.

**Conceptos clave:** Replicación y replication lag · Particionamiento · Niveles de aislamiento · RDS Multi-AZ y réplicas de lectura · DynamoDB y escrituras condicionales

**Autoevaluación:**
1. ¿Multi-AZ de RDS sirve para escalar lecturas?
2. ¿Qué pasa con read-your-writes si lees de una réplica?
3. ¿Cómo evita una escritura condicional la sobreventa?

### Lunes · Teoría · ARQ-501 · Designing Data-Intensive Applications

Capítulos de DDIA sobre replicación, particionamiento y transacciones.

**Pasos:**
1. Replicación (40 min).
2. Particionamiento (35 min).
3. Transacciones y niveles de aislamiento (45 min).

**Terminado cuando:** Explicas replication lag y 2 formas de mitigarlo.

**Recursos:**
  - [O'Reilly: Designing Data-Intensive Applications](https://learning.oreilly.com/search/?q=Designing%20Data-Intensive%20Applications)

### Miércoles · Teoría · CLD-511 · Curso SAA: bases de datos y S3

Secciones de almacenamiento del curso.

**Pasos:**
1. RDS, Aurora y ElastiCache (40 min).
2. DynamoDB (30 min).
3. S3 y S3 avanzado (40 min).
4. Quizzes (10 min).

**Terminado cuando:** Quizzes con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: réplicas, lecturas obsoletas y stock sin sobreventa

Reproduce en AWS los problemas que acabas de leer en DDIA.

**Pasos:**
1. RDS Postgres para Pedidos en subnet privada, con una réplica de lectura.
2. Mide el lag bajo carga y reproduce una lectura obsoleta.
3. Implementa read-your-writes: tras escribir, el usuario lee del primario por unos segundos.
4. DynamoDB para Inventario: reserva con escritura condicional y 50 reservas simultáneas del último producto.

**Terminado cuando:** Muestras la lectura obsoleta, su corrección y un stock que nunca queda negativo.

**Recursos:**
  - [Web: Escrituras condicionales en DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html#WorkingWithItems.ConditionalUpdate)
  - [Web: Réplicas de lectura de RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Estrategia de datos por servicio

Documenta cómo maneja datos cada servicio.

**Pasos:**
1. Tabla por servicio: datos que posee, consistencia requerida, motor, RPO y RTO.
2. Cómo se resuelven consultas entre servicios (API composition o read model con CQRS).
3. ADR-006: bases de datos de la plataforma con mediciones del lab.

**Terminado cuando:** Nota técnica de 1 a 2 páginas y ADR-006.

**Recursos:**
  - [Web: CQRS (Martin Fowler)](https://martinfowler.com/bliki/CQRS.html)

## S07 · Parcial de mitad de semestre · Parcial

**Objetivo:** Medir lo aprendido en las dos materias y estabilizar el proyecto antes de la segunda mitad.

**Conceptos clave:** System design cronometrado · Preguntas tipo examen AWS · Revisión ATAM

**Autoevaluación:**
1. ¿Qué decisión de estas 7 semanas cambiarías hoy?
2. ¿Qué tema de AWS te costó más y cómo lo vas a reforzar?

### Lunes · Examen · ARQ-501 · Parcial ARQ-501: system design

Dos ejercicios cronometrados de 45 minutos cada uno, sin consultar material.

**Pasos:**
1. Ejercicio 1: sistema de notificaciones multicanal (45 min).
2. Ejercicio 2: rate limiter distribuido (45 min).
3. Autocalifica de 1 a 5: requisitos, estimaciones, diseño, trade-offs y cuellos de botella (30 min).

**Terminado cuando:** Promedio de 3,5 o más. Si no, repite un ejercicio en la próxima semana libre.

**Recursos:**
  - [Web: System Design Primer](https://github.com/donnemartin/system-design-primer)

### Miércoles · Examen · CLD-511 · Parcial CLD-511: preguntas tipo examen

Preguntas de práctica solo de los temas vistos: IAM, EC2, VPC, ELB, ASG, ECS, RDS, DynamoDB y S3.

**Pasos:**
1. 40 preguntas en 60 minutos.
2. Revisa cada fallo y anota el concepto que faltó (45 min).
3. Lista de 3 temas a reforzar (15 min).

**Terminado cuando:** 70% o más.

**Recursos:**
  - [Udemy: AWS Certified Solutions Architect Associate practice exams](https://www.udemy.com/courses/search/?q=AWS%20Certified%20Solutions%20Architect%20Associate%20practice%20exams)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: revisión ATAM de lo construido

Evalúa tu arquitectura actual con escenarios de calidad.

**Pasos:**
1. Escribe 6 escenarios (estímulo, entorno, respuesta, medida).
2. Ubica qué decisión soporta cada escenario.
3. Marca puntos de sensibilidad y de trade-off.
4. Agrega los riesgos a la matriz de riesgos.

**Terminado cuando:** Tabla de escenarios y matriz de riesgos actualizada.

**Recursos:**
  - [O'Reilly: ATAM architecture tradeoff analysis method](https://learning.oreilly.com/search/?q=ATAM%20architecture%20tradeoff%20analysis%20method)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Estabilización y retro de mitad de semestre

Paga deuda técnica antes de seguir agregando funcionalidad.

**Pasos:**
1. Cierra los pendientes del proyecto y actualiza los diagramas.
2. Revisa que todos los ADRs sigan siendo ciertos.
3. Retro de mitad de semestre: ritmo, temas difíciles, ajustes al plan.

**Terminado cuando:** Repositorio al día y retro escrita.

## S08 · Eventos y sagas · Mensajería en AWS · Demo v0.2

**Objetivo:** Diseñar flujos distribuidos confiables e implementarlos con servicios de mensajería administrados.

**Conceptos clave:** Coreografía vs. orquestación · Sagas y compensaciones · Transactional Outbox · Consumidor idempotente · SQS, SNS y EventBridge · DLQ y visibility timeout

**Autoevaluación:**
1. ¿Qué problema exacto resuelve el Outbox?
2. ¿Cuándo eliges EventBridge en vez de SNS?
3. ¿Cómo garantizas idempotencia en un consumidor?

### Lunes · Teoría · ARQ-501 · Sagas, contratos y Outbox

Flujo de trabajo distribuido en The Hard Parts y los patrones de confiabilidad de mensajería.

**Pasos:**
1. The Hard Parts: contratos y patrones de saga (60 min).
2. Transactional Outbox e Idempotent Consumer en microservices.io (30 min).
3. Dibuja de memoria una saga con compensación (30 min).

**Terminado cuando:** Explicas 3 tipos de saga y cuándo usar cada uno.

**Recursos:**
  - [O'Reilly: Software Architecture The Hard Parts saga](https://learning.oreilly.com/search/?q=Software%20Architecture%20The%20Hard%20Parts%20saga)
  - [Web: Transactional Outbox](https://microservices.io/patterns/data/transactional-outbox.html)

### Miércoles · Teoría · CLD-511 · Curso SAA: desacoplamiento

Mensajería en AWS con el curso y Serverless Land.

**Pasos:**
1. Sección de SQS, SNS y Kinesis (60 min).
2. EventBridge en el curso y en la documentación (40 min).
3. Patrones de EventBridge con SQS en Serverless Land (20 min).

**Terminado cuando:** Explicas visibility timeout y redrive policy.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Serverless Land patterns](https://serverlessland.com/patterns)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: Outbox hacia EventBridge con consumidor idempotente

Publica eventos de Pedidos de forma confiable y consúmelos en Inventario.

**Pasos:**
1. Tabla outbox en Pedidos y relay que publica a un bus de EventBridge.
2. Regla hacia una cola SQS de Inventario con DLQ (3 reintentos).
3. Inventario registra event_id procesados e ignora duplicados.
4. Prueba: reenvía el mismo evento 5 veces y reinicia el consumidor a mitad de un lote.

**Terminado cuando:** Ningún evento se pierde ni se procesa dos veces.

**Recursos:**
  - [Web: Amazon EventBridge](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Saga coreografiada y Demo v0.2

Implementa el flujo Crear pedido entre servicios.

**Pasos:**
1. Secuencia: PedidoCreado → StockReservado o StockInsuficiente → PagoProcesado o PagoRechazado → PedidoConfirmado.
2. Compensación de cada paso (liberar stock, cancelar pedido).
3. Camino feliz y compensación por pago rechazado funcionando en AWS.
4. Demo v0.2 (3 min): un pedido exitoso y uno compensado.

**Terminado cuando:** Saga funcionando y video de la demo.

## S09 · Resiliencia · Serverless

**Objetivo:** Diseñar servicios que siguen funcionando cuando sus dependencias fallan y usar serverless donde conviene.

**Conceptos clave:** Timeouts, retries con backoff y jitter · Circuit breaker y bulkhead · Lambda: cold starts y concurrencia · API Gateway · Step Functions

**Autoevaluación:**
1. ¿Por qué un retry sin jitter puede tumbar un servicio?
2. ¿Cuándo Lambda sale más caro que Fargate?
3. ¿Qué ventaja da Step Functions para una saga?

### Lunes · Teoría · ARQ-501 · Release It!: patrones de estabilidad

Patrones y antipatrones de estabilidad de Michael Nygard.

**Pasos:**
1. Antipatrones: fallas en cascada, puntos de integración, usuarios (45 min).
2. Patrones: timeouts, circuit breaker, bulkhead, fail fast, steady state (55 min).
3. Tabla patrón → problema que resuelve (20 min).

**Terminado cuando:** Tabla de patrones terminada.

**Recursos:**
  - [O'Reilly: Release It Nygard](https://learning.oreilly.com/search/?q=Release%20It%20Nygard)

### Miércoles · Teoría · CLD-511 · Curso SAA: serverless

Lambda, API Gateway y Step Functions.

**Pasos:**
1. Sección de Lambda (50 min).
2. API Gateway (30 min).
3. Step Functions (30 min).
4. Quizzes (10 min).

**Terminado cuando:** Quizzes con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Step Functions](https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: Notificaciones serverless y resiliencia

Mueve Notificaciones a Lambda y protege las llamadas entre servicios.

**Pasos:**
1. Notificaciones como Lambda disparada por PedidoConfirmado.
2. Circuit breaker, retry con backoff y jitter y timeout en Pedidos → Inventario (Resilience4j, Polly u opossum).
3. Inyecta latencia y errores en Inventario (Toxiproxy local o AWS Fault Injection Service).
4. Verifica que el circuit breaker se abre y se recupera.

**Terminado cuando:** Pedidos responde con degradación controlada mientras Inventario falla.

**Recursos:**
  - [Web: Resilience4j](https://resilience4j.readme.io/)
  - [Web: Polly](https://www.pollydocs.org/)
  - [Web: Toxiproxy](https://github.com/Shopify/toxiproxy)
  - [Web: AWS Fault Injection Service](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Saga orquestada con Step Functions

Implementa la misma saga como orquestación y compara.

**Pasos:**
1. Máquina de estados: reservar stock, cobrar, confirmar.
2. Catch con compensación en cada paso.
3. Prueba el camino de pago rechazado.
4. ADR-007: coreografía vs. orquestación con lo que observaste en ambas.

**Terminado cuando:** Ejecución fallida con compensación visible y ADR-007.

## S10 · Escalabilidad y caché · Rendimiento en AWS

**Objetivo:** Escalar la plataforma con caché y autoescalado, y razonar con estimaciones de capacidad.

**Conceptos clave:** Cache-aside, write-through y TTL · Rate limiting · Estimaciones de capacidad · ElastiCache y CloudFront · Autoescalado de ECS

**Autoevaluación:**
1. ¿Qué problema introduce un caché con TTL largo?
2. Estima instancias para 5.000 solicitudes por segundo.
3. ¿Qué cachearías en CloudFront y qué no?

### Lunes · Teoría · ARQ-501 · Fundamentos de system design

El marco mental de una revisión de system design y las estimaciones de capacidad.

**Pasos:**
1. Videos de ByteByteGo sobre caché, balanceo y rate limiting (50 min).
2. System Design Primer: estimaciones y latencias típicas (40 min).
3. Ejercicio: estima QPS y almacenamiento de la plataforma a 10x usuarios (30 min).

**Terminado cuando:** Estimación de capacidad escrita.

**Recursos:**
  - [YouTube: ByteByteGo system design caching](https://www.youtube.com/results?search_query=ByteByteGo%20system%20design%20caching)
  - [Web: System Design Primer](https://github.com/donnemartin/system-design-primer)

### Miércoles · Teoría · CLD-511 · Curso SAA: caché y entrega de contenido

ElastiCache, CloudFront y Global Accelerator.

**Pasos:**
1. ElastiCache en profundidad (40 min).
2. CloudFront y Global Accelerator (60 min).
3. Quiz (20 min).

**Terminado cuando:** Quiz con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: Catálogo con caché y autoescalado

Acelera el Catálogo y haz que la plataforma escale sola.

**Pasos:**
1. Servicio Catálogo en ECS con cache-aside en ElastiCache Redis e invalidación al actualizar.
2. Prueba de carga con k6: p95 sin caché.
3. Repite con caché y compara.
4. Autoescalado de ECS por CPU o solicitudes; observa cómo sube y baja.

**Terminado cuando:** Tabla de p95 antes y después y autoescalado observado.

**Recursos:**
  - [Web: k6](https://k6.io/docs/)
  - [Web: Autoescalado de ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-auto-scaling.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Diseño a 10x y ADR de caché

Documenta cómo crecería la plataforma.

**Pasos:**
1. Documento: la plataforma con 10x usuarios, cuellos de botella y cómo resolverlos.
2. ADR-008: estrategia de caché con TTL e invalidación.
3. Actualiza el C4 de contenedores.

**Terminado cuando:** Documento de escalabilidad y ADR-008.

## S11 · Observabilidad · Monitoreo en AWS

**Objetivo:** Ver qué pasa dentro de un sistema distribuido y definir cuándo está sano.

**Conceptos clave:** Logs, métricas y trazas · OpenTelemetry · SLI, SLO y presupuesto de error · CloudWatch y X-Ray · CloudTrail

**Autoevaluación:**
1. ¿Qué diferencia un SLO de un SLA?
2. ¿Por qué las trazas son más útiles que los logs en sistemas distribuidos?
3. ¿Qué es un presupuesto de error y para qué sirve?

### Lunes · Teoría · ARQ-501 · Observability Engineering

Fundamentos de observabilidad moderna.

**Pasos:**
1. Capítulos 1 a 4: observabilidad y eventos estructurados (45 min).
2. Capítulos sobre trazas distribuidas y OpenTelemetry (45 min).
3. Capítulo de SLOs (30 min).

**Terminado cuando:** Defines 2 SLOs con su SLI para la plataforma.

**Recursos:**
  - [O'Reilly: Observability Engineering](https://learning.oreilly.com/search/?q=Observability%20Engineering)

### Miércoles · Teoría · CLD-511 · Curso SAA: monitoreo y auditoría

CloudWatch, X-Ray y CloudTrail, más la distribución de OpenTelemetry de AWS.

**Pasos:**
1. Sección de monitoreo y auditoría (70 min).
2. Documentación de ADOT (30 min).
3. Quiz (20 min).

**Terminado cuando:** Quiz con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: ADOT](https://aws-otel.github.io/)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: trazas de la saga completa

Instrumenta la plataforma para seguir un pedido de punta a punta.

**Pasos:**
1. SDK de OpenTelemetry en Pedidos, Inventario y Catálogo.
2. Instrumentación de la Lambda de Notificaciones.
3. Propagación de contexto a través de EventBridge y SQS.
4. Encuentra en X-Ray la traza de un pedido que cruza todos los servicios.

**Terminado cuando:** Una sola traza muestra la saga completa.

**Recursos:**
  - [Web: OpenTelemetry](https://opentelemetry.io/docs/)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · SLOs, alarmas y runbook

Define cuándo la plataforma está sana y qué hacer cuando no.

**Pasos:**
1. Dashboard de CloudWatch con 2 SLOs (disponibilidad y latencia p95).
2. 3 alarmas accionables.
3. Runbook inicial: qué revisar ante cada alarma.

**Terminado cuando:** Dashboard, alarmas y runbook en el repo.

## S12 · Seguridad por diseño · Seguridad en AWS · Demo v0.3

**Objetivo:** Modelar amenazas desde el diseño y aplicar defensa en profundidad en AWS.

**Conceptos clave:** Threat modeling STRIDE · Defensa en profundidad · KMS y Secrets Manager · WAF y Shield · Cognito · Privilegio mínimo

**Autoevaluación:**
1. Da un ejemplo de cada letra de STRIDE en la plataforma.
2. ¿Por qué cada task de ECS debe tener su propio rol?
3. ¿Qué protege WAF que no protegen los Security Groups?

### Lunes · Teoría · ARQ-501 · Threat modeling

Modelado de amenazas para arquitectos.

**Pasos:**
1. Libro Threat Modeling (Tarandach y Coles): fundamentos y STRIDE (60 min).
2. OWASP Threat Modeling Cheat Sheet (30 min).
3. Lista de activos y fronteras de confianza de la plataforma (30 min).

**Terminado cuando:** Diagrama de flujo de datos con fronteras de confianza.

**Recursos:**
  - [O'Reilly: Threat Modeling Tarandach](https://learning.oreilly.com/search/?q=Threat%20Modeling%20Tarandach)
  - [Web: OWASP Threat Modeling](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

### Miércoles · Teoría · CLD-511 · Curso SAA: seguridad y cifrado

KMS, Secrets Manager, WAF, Shield y Cognito.

**Pasos:**
1. Sección de seguridad y cifrado (70 min).
2. Cognito (30 min).
3. Quiz (20 min).

**Terminado cuando:** Quiz con 80% o más.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: endurecer la plataforma

Aplica lo leído sobre la plataforma desplegada.

**Pasos:**
1. Credenciales de base de datos en Secrets Manager, rotación activada.
2. Un rol IAM por task de ECS con permisos mínimos.
3. WAF en el ALB con reglas administradas.
4. Autenticación JWT con Cognito en la API.
5. Prueba que un rol no puede acceder a recursos de otro servicio.

**Terminado cuando:** Accesos indebidos rechazados y ningún secreto en código o variables planas.

**Recursos:**
  - [Web: Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)
  - [Web: AWS WAF](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Threat model y Demo v0.3

Documenta la seguridad de la plataforma.

**Pasos:**
1. Threat model STRIDE con amenazas, riesgo y mitigación.
2. ADR-009: autenticación y autorización.
3. Demo v0.3 (3 min): resiliencia, caché, trazas y seguridad.

**Terminado cuando:** Threat model, ADR-009 y video.

## S13 · Arquitectura evolutiva · CI/CD en AWS

**Objetivo:** Proteger la arquitectura mientras cambia y desplegar sin intervención manual.

**Conceptos clave:** Fitness functions · Arquitectura evolutiva · GitHub Actions · OIDC con AWS · Rolling y blue/green

**Autoevaluación:**
1. Da 3 ejemplos de fitness functions para la plataforma.
2. ¿Por qué OIDC es mejor que guardar llaves de AWS en GitHub?
3. ¿Qué riesgo tiene un despliegue rolling?

### Lunes · Teoría · ARQ-501 · Building Evolutionary Architectures

Arquitectura evolutiva y fitness functions (2.ª edición).

**Pasos:**
1. Fitness functions: tipos y ejemplos (50 min).
2. Cambio incremental y acoplamiento (40 min).
3. Diseña 5 fitness functions para la plataforma (30 min).

**Terminado cuando:** Lista de 5 fitness functions con cómo automatizarlas.

**Recursos:**
  - [O'Reilly: Building Evolutionary Architectures](https://learning.oreilly.com/search/?q=Building%20Evolutionary%20Architectures)

### Miércoles · Teoría · CLD-511 · CI/CD hacia ECS

GitHub Actions, OIDC y estrategias de despliegue en ECS.

**Pasos:**
1. GitHub Actions: workflows, environments y secretos (40 min).
2. OIDC entre GitHub y AWS (30 min).
3. Rolling y blue/green en ECS con CodeDeploy (50 min).

**Terminado cuando:** Sabes configurar el rol de confianza para OIDC.

**Recursos:**
  - [Web: OIDC de GitHub con AWS](https://docs.github.com/en/actions/security-for-github-actions/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services)
  - [YouTube: GitHub Actions deploy ECS](https://www.youtube.com/results?search_query=GitHub%20Actions%20deploy%20ECS)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Lab: pipeline con fitness functions

Automatiza el despliegue con controles de arquitectura.

**Pasos:**
1. Pipeline: tests → fitness functions → contract tests → build → escaneo de imagen → ECR → ECS.
2. Autenticación a AWS por OIDC, sin llaves.
3. Fitness function de latencia: prueba k6 corta que falla si el p95 empeora.
4. Prueba: rompe una regla de dependencias y verifica que el pipeline se detiene.

**Terminado cuando:** Un push a main despliega solo y una violación de arquitectura bloquea el despliegue.

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Documento de arquitectura completo

Prepara la entrega del semestre.

**Pasos:**
1. Integra en un documento: visión, características, C4, context map, ADRs, datos, saga, escalabilidad, seguridad, observabilidad.
2. Matriz de riesgos y deuda técnica.
3. Revisa contra los requisitos del proyecto integrador.

**Terminado cuando:** Borrador final del documento.

**Recursos:**
  - [Web: arc42](https://arc42.org/overview)

## S14 · Final del semestre 1 · Final

**Objetivo:** Cerrar el semestre con exámenes y la entrega de la plataforma v1.0.

**Conceptos clave:** System design · Preguntas tipo SAA · Defensa de arquitectura

**Autoevaluación:**
1. ¿Cuál es el riesgo más alto de tu arquitectura hoy?
2. ¿Qué dominio del examen SAA es tu punto débil?

### Lunes · Examen · ARQ-501 · Final ARQ-501: system design

Dos ejercicios cronometrados sin consultar material.

**Pasos:**
1. Ejercicio 1: feed de noticias (45 min).
2. Ejercicio 2: sistema de reservas con alta concurrencia (45 min).
3. Autocalificación con la rúbrica del parcial (30 min).

**Terminado cuando:** Promedio de 3,5 o más.

**Recursos:**
  - [Web: System Design Primer](https://github.com/donnemartin/system-design-primer)

### Miércoles · Examen · CLD-511 · Final CLD-511: simulacro de temas vistos

Preguntas tipo examen de todo lo visto en el semestre.

**Pasos:**
1. 50 preguntas en 75 minutos.
2. Análisis de fallos por dominio del examen (30 min).
3. Plan de refuerzo para el semestre 2 (15 min).

**Terminado cuando:** 72% o más.

**Recursos:**
  - [Udemy: AWS Certified Solutions Architect Associate practice exams](https://www.udemy.com/courses/search/?q=AWS%20Certified%20Solutions%20Architect%20Associate%20practice%20exams)

### Viernes · Laboratorio integrado · ARQ-501 + CLD-511 · Ensayo de defensa y ATAM final

Prepárate para presentar.

**Pasos:**
1. Revisión ATAM final con los escenarios de la semana 7.
2. Ensaya la explicación de 5 minutos de la arquitectura.
3. Lista de preguntas difíciles que te harían y sus respuestas.

**Terminado cuando:** Explicación ensayada en menos de 5 minutos.

### Sábado · Proyecto integrador · ARQ-501 + CLD-511 · Entrega del proyecto integrador v1.0

Entrega la plataforma diseñada y desplegada. Revisa requisitos y rúbrica en Proyecto integrador.

**Pasos:**
1. Completa los requisitos pendientes.
2. Demo grabada de 5 minutos.
3. Autoevalúate con la rúbrica.
4. Etiqueta v1.0 y retro del semestre.

**Terminado cuando:** Etiqueta v1.0 y rúbrica con 75 puntos o más.

---

# SEM 2 · Datos de la plataforma (semanas 15 a 29)

La plataforma empieza a generar valor con sus datos mientras la infraestructura pasa a código. Incluye la materia corta de matemáticas y la certificación AWS en la semana 22.

**Materias:** DAT-521 Ciencia e Ingeniería de Datos · CLD-512 Cloud II: Plataforma, Operación y Certificación

**Hitos:** S18 Demo v1.1 · S22 Parcial y certificación AWS · S23 Demo v1.2 · S26 Demo v1.3 · S29 Final y entrega v2.0

## S15 · Python para datos · Terraform

**Objetivo:** Manipular datos con fluidez y empezar a describir la infraestructura como código.

**Conceptos clave:** NumPy y vectorización · DataFrames, groupby, merge · Parquet · Providers y recursos · Ciclo init, plan, apply

**Autoevaluación:**
1. ¿Por qué un loop de Python sobre un DataFrame es mala idea?
2. ¿Por qué Parquet es mejor que CSV para análisis?
3. ¿Qué hace terraform plan?

### Lunes · Teoría · DAT-521 · Python for Data Analysis y pandas

Capítulos centrales de Wes McKinney y el curso de pandas de Kaggle.

**Pasos:**
1. NumPy y estructuras de pandas (40 min).
2. Carga, limpieza y transformación de datos (40 min).
3. Kaggle Learn: pandas, primeras 3 lecciones (40 min).

**Terminado cuando:** Ejecutaste los ejemplos en tu notebook.

**Recursos:**
  - [O'Reilly: Python for Data Analysis McKinney](https://learning.oreilly.com/search/?q=Python%20for%20Data%20Analysis%20McKinney)
  - [Web: Kaggle Learn: Pandas](https://www.kaggle.com/learn/pandas)

### Miércoles · Teoría · CLD-512 · Terraform: Up and Running, caps. 1 a 3

Fundamentos de infraestructura como código con Yevgeniy Brikman.

**Pasos:**
1. Por qué IaC y cómo empezar con Terraform (50 min).
2. Estado de Terraform (40 min).
3. Curso de Terraform en Platzi o Udemy: primeras secciones (30 min).

**Terminado cuando:** Explicas qué es el estado y por qué no va en Git.

**Recursos:**
  - [O'Reilly: Terraform Up and Running](https://learning.oreilly.com/search/?q=Terraform%20Up%20and%20Running)
  - [Platzi: terraform](https://platzi.com/buscar/?search=terraform)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: dataset sintético hacia S3 con Terraform

Genera datos realistas y crea tu primer recurso con Terraform.

**Pasos:**
1. Con Faker: 5.000 clientes, 300 productos en 8 categorías y 100.000 pedidos en 2 años.
2. Agrega estacionalidad, cancelaciones del 8% y algo de suciedad (nulos, duplicados, precios atípicos).
3. Bucket S3 raw creado con Terraform, cifrado y sin acceso público.
4. Sube los datos en Parquet.

**Terminado cuando:** Bucket creado por Terraform con los 3 archivos Parquet.

**Recursos:**
  - [Web: Faker](https://faker.readthedocs.io/)
  - [Web: Terraform AWS provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Red de la plataforma en Terraform

Empieza a migrar la plataforma a código.

**Pasos:**
1. Módulo de red: VPC, subnets, gateways y tablas de rutas.
2. Variables por entorno.
3. Crea la red nueva y verifica rutas.
4. Plan para mover los servicios a la red nueva.

**Terminado cuando:** La red de la plataforma existe solo como código.

## S16 · Estadística descriptiva · Módulos y estado

**Objetivo:** Describir datos correctamente y organizar Terraform para un sistema real.

**Conceptos clave:** Media, mediana y percentiles · Distribuciones · Bootstrap · Módulos de Terraform · Estado remoto y locking

**Autoevaluación:**
1. ¿Cuándo la mediana describe mejor que la media?
2. ¿Qué te dice un intervalo de confianza del 95%?
3. ¿Qué pasa si dos personas aplican sin lock?

### Lunes · Teoría · DAT-521 · Practical Statistics, caps. 1 y 2

Estadística orientada a la práctica, con videos de StatQuest de apoyo.

**Pasos:**
1. Capítulo 1: análisis exploratorio (50 min).
2. Capítulo 2: distribuciones y muestreo (50 min).
3. StatQuest: bootstrapping (20 min).

**Terminado cuando:** Explicas el bootstrap sin fórmulas.

**Recursos:**
  - [O'Reilly: Practical Statistics for Data Scientists](https://learning.oreilly.com/search/?q=Practical%20Statistics%20for%20Data%20Scientists)
  - [YouTube: StatQuest bootstrapping](https://www.youtube.com/results?search_query=StatQuest%20bootstrapping)

### Miércoles · Teoría · CLD-512 · Terraform: módulos y estado remoto

Capítulos 4 a 6 de Terraform: Up and Running.

**Pasos:**
1. Módulos (40 min).
2. Trucos: loops, condicionales y despliegues sin caída (40 min).
3. Manejo de secretos (20 min).
4. Ejercicios del curso (20 min).

**Terminado cuando:** Sabes estructurar módulos y entornos.

**Recursos:**
  - [O'Reilly: Terraform Up and Running modules](https://learning.oreilly.com/search/?q=Terraform%20Up%20and%20Running%20modules)
  - [Web: Backend S3](https://developer.hashicorp.com/terraform/language/backend/s3)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: limpieza y distribuciones

Limpia los datos y describe el negocio.

**Pasos:**
1. Notebook de limpieza: tipos, nulos, duplicados y atípicos, justificando cada decisión.
2. Histograma y boxplot del valor de pedido; compáralo con una log-normal.
3. Percentiles por categoría.
4. Bootstrap del ticket promedio con intervalo de confianza.

**Terminado cuando:** Notebook que corre de principio a fin con interpretación escrita.

**Recursos:**
  - [Web: SciPy stats](https://docs.scipy.org/doc/scipy/reference/stats.html)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Servicios en módulos de Terraform

Continúa la migración a código.

**Pasos:**
1. Módulos de ECS, RDS, DynamoDB, EventBridge y SQS.
2. Estado remoto en S3 con locking.
3. Despliega los servicios en la red nueva y destruye la infraestructura manual.

**Terminado cuando:** Servicios corriendo sobre infraestructura creada por Terraform.

## S17 · Inferencia y A/B testing · SAA: arquitecturas seguras

**Objetivo:** Tomar decisiones con experimentos y empezar la preparación de la certificación por dominios.

**Conceptos clave:** p-value y significancia · Potencia y tamaño de muestra · Peeking · Dominio de diseño seguro del examen · IAM avanzado, KMS, organizaciones

**Autoevaluación:**
1. ¿Qué NO significa un p-value de 0,03?
2. ¿Por qué detener un test apenas sale significativo es un error?
3. ¿Qué son las SCP de AWS Organizations?

### Lunes · Teoría · DAT-521 · Practical Statistics, capítulo 3

Experimentos estadísticos y pruebas de significancia.

**Pasos:**
1. A/B testing y pruebas de hipótesis (40 min).
2. Potencia y tamaño de muestra (40 min).
3. StatQuest: p-values y análisis de potencia (40 min).

**Terminado cuando:** Calculas el tamaño de muestra de un A/B.

**Recursos:**
  - [O'Reilly: Practical Statistics for Data Scientists](https://learning.oreilly.com/search/?q=Practical%20Statistics%20for%20Data%20Scientists)
  - [YouTube: StatQuest p-values](https://www.youtube.com/results?search_query=StatQuest%20p-values)
  - [YouTube: StatQuest power analysis](https://www.youtube.com/results?search_query=StatQuest%20power%20analysis)

### Miércoles · Teoría · CLD-512 · SAA: dominio de arquitecturas seguras

Repaso por dominio del examen. Agenda el examen para la semana 22 esta semana.

**Pasos:**
1. Revisa la guía del examen y agenda la fecha (15 min).
2. Repasa las secciones de seguridad, IAM avanzado y Organizations (60 min).
3. 30 preguntas de práctica del dominio (45 min).

**Terminado cuando:** Examen agendado y 70% o más en el dominio.

**Recursos:**
  - [Web: Guía del examen SAA](https://aws.amazon.com/certification/certified-solutions-architect-associate/)
  - [Udemy: AWS Certified Solutions Architect Associate practice exams](https://www.udemy.com/courses/search/?q=AWS%20Certified%20Solutions%20Architect%20Associate%20practice%20exams)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: A/B test del checkout

Simula que el checkout nuevo sube la conversión de 3,0% a 3,4%.

**Pasos:**
1. Tamaño de muestra para potencia 80% y alfa 5% con statsmodels.
2. Prueba z de proporciones e intervalo de la diferencia.
3. Repite 1.000 simulaciones y mide cuántas veces detectas el efecto.
4. Simula el peeking diario y mide los falsos positivos.

**Terminado cuando:** Notebook que muestra la potencia real y el daño del peeking.

**Recursos:**
  - [Web: statsmodels: potencia](https://www.statsmodels.org/stable/stats.html#power-and-sample-size-calculations)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Terraform completo con plan en pull request

La infraestructura se revisa como el código.

**Pasos:**
1. GitHub Actions con fmt, validate, tflint, checkov y plan en cada PR.
2. Comentario automático del plan.
3. terraform destroy y apply de todo el entorno dev.
4. ADR-010: estructura de Terraform y entornos.

**Terminado cuando:** Entorno recreado sin pasos manuales y ADR-010.

**Recursos:**
  - [Web: tflint](https://github.com/terraform-linters/tflint)
  - [Web: Checkov](https://www.checkov.io/)

## S18 · Álgebra lineal · SAA: arquitecturas resilientes · Demo v1.1

**Objetivo:** Recuperar el álgebra lineal que usan los modelos y dominar la resiliencia en AWS.

**Conceptos clave:** Vectores, matrices y producto punto · Matrices como transformaciones · Estrategias de recuperación ante desastres · Multi-AZ y multi-región · Backups

**Autoevaluación:**
1. ¿Qué representa geométricamente el producto punto?
2. Diferencia entre pilot light y warm standby.
3. ¿Qué RTO tiene un backup and restore?

### Lunes · Teoría · MAT-523 · Essence of Linear Algebra

Teoría en video, la mejor forma de recuperar la intuición geométrica, más la primera semana del curso de Imperial College.

**Pasos:**
1. 3Blue1Brown, capítulos 1 a 9 (70 min).
2. Mathematics for Machine Learning: Linear Algebra, semana 1 (50 min).

**Terminado cuando:** Explicas una multiplicación de matrices como composición de transformaciones.

**Recursos:**
  - [YouTube: 3Blue1Brown Essence of linear algebra](https://www.youtube.com/results?search_query=3Blue1Brown%20Essence%20of%20linear%20algebra)
  - [Coursera: Mathematics for Machine Learning Imperial College](https://www.coursera.org/search?query=Mathematics%20for%20Machine%20Learning%20Imperial%20College)

### Miércoles · Teoría · CLD-512 · SAA: dominio de arquitecturas resilientes

Alta disponibilidad, recuperación ante desastres y backups.

**Pasos:**
1. Repasa la sección de recuperación ante desastres y migraciones (60 min).
2. Whitepaper de estrategias de DR de AWS (20 min).
3. 30 preguntas del dominio (40 min).

**Terminado cuando:** 70% o más en el dominio.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Estrategias de DR en AWS](https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html)

### Viernes · Laboratorio integrado · MAT-523 · Lab: álgebra lineal con NumPy

Lleva la intuición a código.

**Pasos:**
1. Producto punto, normas y proyecciones.
2. Multiplicación de matrices y transformaciones de puntos 2D graficadas.
3. Regresión lineal con la ecuación normal sobre los datos de pedidos.
4. Compara con scikit-learn.

**Terminado cuando:** Tus coeficientes coinciden con los de scikit-learn.

**Recursos:**
  - [Web: NumPy linalg](https://numpy.org/doc/stable/reference/routines.linalg.html)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Exportación diaria al data lake y Demo v1.1

La plataforma empieza a alimentar el lake.

**Pasos:**
1. Tarea programada (ECS scheduled task o Lambda) que exporta los pedidos del día a S3 raw en Parquet, particionado por fecha.
2. Todo en Terraform.
3. Demo v1.1 (3 min): Terraform, A/B test y datos llegando al lake.

**Terminado cuando:** Archivos diarios en S3 y video de la demo.

## S19 · Cálculo y descenso de gradiente · SAA: alto rendimiento

**Objetivo:** Entender cómo aprende un modelo y elegir servicios por rendimiento.

**Conceptos clave:** Derivadas y regla de la cadena · Gradiente · Descenso de gradiente y tasa de aprendizaje · Rendimiento de almacenamiento y bases de datos · Rendimiento de red

**Autoevaluación:**
1. ¿Por qué el gradiente apunta a la dirección de mayor crecimiento?
2. ¿Qué pasa con una tasa de aprendizaje muy alta?
3. ¿Cuándo eliges io2 sobre gp3?

### Lunes · Teoría · MAT-523 · Essence of Calculus y cálculo multivariable

Intuición de derivadas y gradientes.

**Pasos:**
1. 3Blue1Brown, Essence of Calculus, capítulos 1 a 4 (50 min).
2. Mathematics for ML: Multivariate Calculus, semanas 1 y 2 (70 min).

**Terminado cuando:** Explicas la regla de la cadena con un ejemplo.

**Recursos:**
  - [YouTube: 3Blue1Brown Essence of calculus](https://www.youtube.com/results?search_query=3Blue1Brown%20Essence%20of%20calculus)
  - [Coursera: Mathematics for Machine Learning Multivariate Calculus](https://www.coursera.org/search?query=Mathematics%20for%20Machine%20Learning%20Multivariate%20Calculus)

### Miércoles · Teoría · CLD-512 · SAA: dominio de alto rendimiento

Elegir cómputo, almacenamiento, bases y red por rendimiento.

**Pasos:**
1. Repasa EBS, EFS, FSx y tipos de instancia (50 min).
2. Repasa Aurora, DynamoDB DAX y ElastiCache (30 min).
3. 30 preguntas del dominio (40 min).

**Terminado cuando:** 70% o más en el dominio.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · MAT-523 · Lab: descenso de gradiente a mano

Implementa la optimización que usan todos los modelos.

**Pasos:**
1. Regresión lineal con descenso de gradiente escrito a mano.
2. Grafica la pérdida con 3 tasas de aprendizaje.
3. Versión estocástica por lotes.
4. Cheatsheet de 2 páginas: álgebra lineal, cálculo y descenso de gradiente.

**Terminado cuando:** Converge al mismo resultado que la ecuación normal y tienes el cheatsheet.

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Resumen estadístico e informe del A/B

Comunica los primeros hallazgos como lo haría un equipo de producto.

**Pasos:**
1. 5 hallazgos del negocio con un número y una visualización cada uno.
2. Informe del A/B: hipótesis, resultado con intervalo, recomendación.
3. README del área de datos.

**Terminado cuando:** Informe de 2 páginas.

## S20 · Modelado de datos y ELT · SAA: optimización de costos

**Objetivo:** Construir modelos analíticos confiables y diseñar arquitecturas de costo eficiente.

**Conceptos clave:** OLTP vs. OLAP · Hechos y dimensiones · ELT con dbt · Savings Plans e instancias spot · Clases de almacenamiento

**Autoevaluación:**
1. ¿Qué es la granularidad de una tabla de hechos?
2. ¿Por qué no se hace analítica sobre la base de Pedidos?
3. ¿Cuándo usarías spot?

### Lunes · Teoría · DAT-521 · Fundamentals of Data Engineering y dbt

Ciclo de vida de la ingeniería de datos y modelado.

**Pasos:**
1. FDE: ciclo de vida y corrientes subyacentes (50 min).
2. FDE: consultas, modelado y transformación (40 min).
3. dbt Fundamentals: modelos, fuentes y tests (30 min).

**Terminado cuando:** Describes el ciclo de vida con un ejemplo de la plataforma.

**Recursos:**
  - [O'Reilly: Fundamentals of Data Engineering](https://learning.oreilly.com/search/?q=Fundamentals%20of%20Data%20Engineering)
  - [Web: dbt Learn](https://learn.getdbt.com/)

### Miércoles · Teoría · CLD-512 · SAA: dominio de costos

Optimización de costos en AWS.

**Pasos:**
1. Repasa modelos de precio, Savings Plans, spot y clases de S3 (50 min).
2. Cost Explorer y presupuestos (20 min).
3. 30 preguntas del dominio (50 min).

**Terminado cuando:** 70% o más en el dominio.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: modelo estrella con dbt

Transforma los datos limpios en un modelo dimensional.

**Pasos:**
1. Proyecto dbt con DuckDB leyendo los Parquet.
2. Modelos staging.
3. fct_pedidos (granularidad: línea de pedido), dim_cliente, dim_producto, dim_fecha.
4. Tests unique, not_null, relationships y uno personalizado.

**Terminado cuando:** dbt build verde.

**Recursos:**
  - [Web: dbt-duckdb](https://github.com/duckdb/dbt-duckdb)
  - [Web: DuckDB](https://duckdb.org/docs/)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Modelo documentado

Publica el modelo como lo encontraría un analista nuevo.

**Pasos:**
1. Descripciones de modelos y columnas.
2. dbt docs con linaje.
3. 3 consultas de negocio de ejemplo.
4. ADR-011: almacén analítico (DuckDB local vs. Athena).

**Terminado cuando:** Documentación navegable y ADR-011.

## S21 · Pipelines y orquestación · Simulacro SAA

**Objetivo:** Automatizar el flujo de datos y medirte en un examen completo.

**Conceptos clave:** Orquestación · Idempotencia en pipelines · Backfills · Pruebas de calidad de datos · Simulacro completo

**Autoevaluación:**
1. ¿Qué hace idempotente a una tarea de un pipeline?
2. ¿Qué es un backfill?
3. ¿Qué dominio del examen te sale peor?

### Lunes · Teoría · DAT-521 · Orquestación de datos

Segunda parte de Fundamentals of Data Engineering y el curso de Airflow.

**Pasos:**
1. FDE: orquestación y DataOps (40 min).
2. Curso de Airflow: DAGs, tareas, scheduler, reintentos (60 min).
3. Prefect como alternativa más liviana (20 min).

**Terminado cuando:** Corriste un DAG de ejemplo en local.

**Recursos:**
  - [O'Reilly: Fundamentals of Data Engineering](https://learning.oreilly.com/search/?q=Fundamentals%20of%20Data%20Engineering)
  - [Udemy: Apache Airflow hands-on introduction Marc Lamberti](https://www.udemy.com/courses/search/?q=Apache%20Airflow%20hands-on%20introduction%20Marc%20Lamberti)
  - [Web: Prefect](https://docs.prefect.io/)

### Miércoles · Examen · CLD-512 · Simulacro SAA completo 1

Examen de práctica en condiciones reales: 65 preguntas, 130 minutos, sin consultar.

**Pasos:**
1. Haz el simulacro completo.
2. Anota cada fallo con el concepto que faltó.

**Terminado cuando:** 72% o más. Si no, dedica la semana 22 a esos temas.

**Recursos:**
  - [Udemy: AWS Certified Solutions Architect Associate practice exams](https://www.udemy.com/courses/search/?q=AWS%20Certified%20Solutions%20Architect%20Associate%20practice%20exams)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: DAG de la plataforma

Orquesta el flujo de datos diario.

**Pasos:**
1. Airflow en Docker (o Prefect).
2. DAG: extraer de RDS → S3 raw → dbt build → pruebas de calidad.
3. Tareas idempotentes: correr dos veces el mismo día no duplica.
4. Alerta si falla una prueba de calidad.

**Terminado cuando:** El DAG corre completo y es idempotente.

**Recursos:**
  - [Web: Airflow docs](https://airflow.apache.org/docs/)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Pipeline de punta a punta con backfill

Deja el pipeline listo para producción.

**Pasos:**
1. Backfill de 30 días sin duplicados.
2. Documenta el DAG y su runbook.
3. Diagrama del flujo de datos en el C4.

**Terminado cuando:** Backfill verificado y documentación lista.

## S22 · Parcial y certificación AWS · Parcial y certificación

**Objetivo:** Medir el avance en datos y presentar la certificación AWS Solutions Architect Associate.

**Conceptos clave:** Análisis cronometrado · Simulacro final · Examen de certificación

**Autoevaluación:**
1. ¿Qué parte del ejercicio de datos te tomó más tiempo?
2. ¿Qué harías distinto en la preparación del examen?

### Lunes · Examen · DAT-521 · Parcial DAT-521: análisis cronometrado

Ejercicio de 2 horas con un dataset que no conoces (por ejemplo, uno público de Kaggle).

**Pasos:**
1. Limpieza y análisis exploratorio (50 min).
2. Una prueba de hipótesis bien planteada (40 min).
3. Informe de 1 página (30 min).

**Terminado cuando:** Informe con conclusión respaldada por la prueba.

**Recursos:**
  - [Web: Datasets de Kaggle](https://www.kaggle.com/datasets)

### Miércoles · Examen · CLD-512 · Simulacro SAA completo 2

Último simulacro antes del examen.

**Pasos:**
1. Simulacro completo de 65 preguntas (sin pasarte de 2 h; termina el resto el jueves si hace falta).
2. Revisa los fallos.

**Terminado cuando:** 75% o más.

**Recursos:**
  - [Udemy: AWS Certified Solutions Architect Associate practice exams](https://www.udemy.com/courses/search/?q=AWS%20Certified%20Solutions%20Architect%20Associate%20practice%20exams)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Repaso final de puntos débiles

Sesión liviana: no aprendas temas nuevos.

**Pasos:**
1. Repasa solo los conceptos que fallaste en los simulacros.
2. Lee las preguntas frecuentes de 3 servicios clave.
3. Revisa requisitos del examen en línea o presencial.

**Terminado cuando:** Lista corta de recordatorios para el examen.

### Sábado · Certificación · DAT-521 + CLD-512 · Presentar el examen AWS SAA

El examen dura 130 minutos. Si es en línea, prepara el espacio según las reglas del proveedor.

**Pasos:**
1. Llega o conéctate 30 minutos antes.
2. Marca las preguntas dudosas y vuelve al final.
3. Después, anota los temas que te sorprendieron.
4. Si no apruebas, agenda el reintento a 14 días y enfoca el estudio en tus dominios débiles.

**Terminado cuando:** Examen presentado.

**Recursos:**
  - [Web: Guía del examen SAA](https://aws.amazon.com/certification/certified-solutions-architect-associate/)

## S23 · Machine learning supervisado · Kubernetes · Demo v1.2

**Objetivo:** Entrenar y evaluar bien un modelo de clasificación y entender Kubernetes.

**Conceptos clave:** Train, validation y test · Regresión logística · Precision, recall, ROC-AUC · Data leakage · Pods, Deployments y Services

**Autoevaluación:**
1. ¿Por qué accuracy engaña con clases desbalanceadas?
2. Da un ejemplo de leakage en cancelaciones.
3. ¿Qué pasa si no defines readiness probe?

### Lunes · Teoría · DAT-521 · Hands-On Machine Learning, caps. 1 a 4

Primeros capítulos de Aurélien Géron. Como apoyo, el curso 1 de la especialización de Andrew Ng.

**Pasos:**
1. Panorama del ML (20 min).
2. Proyecto de punta a punta (50 min).
3. Clasificación y métricas (30 min).
4. Entrenamiento y regularización (20 min).

**Terminado cuando:** Ejecutaste el proyecto del capítulo 2.

**Recursos:**
  - [O'Reilly: Hands-On Machine Learning Geron](https://learning.oreilly.com/search/?q=Hands-On%20Machine%20Learning%20Geron)
  - [Coursera: Machine Learning Specialization Andrew Ng](https://www.coursera.org/search?query=Machine%20Learning%20Specialization%20Andrew%20Ng)

### Miércoles · Teoría · CLD-512 · Kubernetes: Up and Running

Objetos esenciales de Kubernetes con los laboratorios del curso de Mumshad.

**Pasos:**
1. Pods, labels, Services y Deployments en el libro (60 min).
2. Laboratorios en el navegador del curso (60 min).

**Terminado cuando:** Escribes un Deployment y un Service sin copiar.

**Recursos:**
  - [O'Reilly: Kubernetes Up and Running](https://learning.oreilly.com/search/?q=Kubernetes%20Up%20and%20Running)
  - [Udemy: Kubernetes for the Absolute Beginners Mumshad](https://www.udemy.com/courses/search/?q=Kubernetes%20for%20the%20Absolute%20Beginners%20Mumshad)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: modelo de cancelación

Predice qué pedidos se van a cancelar con los datos curados.

**Pasos:**
1. Features disponibles al crear el pedido (sin leakage).
2. Split temporal: entrena con meses antiguos, prueba con recientes.
3. Pipeline de scikit-learn con regresión logística y baseline trivial.
4. Matriz de confusión, precision, recall y ROC-AUC.

**Terminado cuando:** El modelo supera claramente al baseline.

**Recursos:**
  - [Web: scikit-learn pipelines](https://scikit-learn.org/stable/modules/compose.html)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Notebook del modelo y Demo v1.2

Documenta el modelo y muestra el avance.

**Pasos:**
1. Problema, métrica, features y riesgos de leakage descartados.
2. Umbral de decisión recomendado.
3. Demo v1.2 (3 min): pipeline diario y primer modelo.

**Terminado cuando:** Notebook y video.

## S24 · Árboles y ensembles · Helm y EKS

**Objetivo:** Usar los modelos que ganan en datos tabulares y empaquetar servicios para Kubernetes.

**Conceptos clave:** Árboles de decisión · Random forest y boosting · Validación cruzada y búsqueda de hiperparámetros · SHAP · Helm · EKS vs. ECS

**Autoevaluación:**
1. ¿Por qué boosting suele ganarle a random forest en tabulares?
2. ¿Qué te dice un valor SHAP?
3. ¿Cuándo justificarías EKS sobre ECS?

### Lunes · Teoría · DAT-521 · Hands-On ML, caps. 6 y 7

Árboles y ensembles, con el curso 2 de Andrew Ng como apoyo.

**Pasos:**
1. Árboles de decisión (40 min).
2. Ensembles, bagging y boosting (50 min).
3. Ng: consejos para aplicar ML, bias y varianza (30 min).

**Terminado cuando:** Explicas bagging vs. boosting.

**Recursos:**
  - [O'Reilly: Hands-On Machine Learning Geron ensemble](https://learning.oreilly.com/search/?q=Hands-On%20Machine%20Learning%20Geron%20ensemble)
  - [Coursera: Machine Learning Specialization Advanced Learning Algorithms](https://www.coursera.org/search?query=Machine%20Learning%20Specialization%20Advanced%20Learning%20Algorithms)

### Miércoles · Teoría · CLD-512 · Helm y EKS

Empaquetado con Helm y Kubernetes administrado en AWS.

**Pasos:**
1. Documentación de Helm: charts, values y templates (50 min).
2. Curso de Mumshad: sección de Helm o deployments (40 min).
3. Comparación ECS vs. EKS en costo y operación (30 min).

**Terminado cuando:** Sabes crear un chart con values por entorno.

**Recursos:**
  - [Web: Helm docs](https://helm.sh/docs/)
  - [Web: Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: XGBoost, Optuna y SHAP

Mejora el modelo de cancelación.

**Pasos:**
1. XGBoost o LightGBM con validación cruzada temporal.
2. Optuna con 30 intentos.
3. SHAP: las 10 variables más influyentes.
4. Comparativa contra la regresión logística.

**Terminado cuando:** Mejora medible y explicada.

**Recursos:**
  - [Web: XGBoost](https://xgboost.readthedocs.io/)
  - [Web: Optuna](https://optuna.org/)
  - [Web: SHAP](https://shap.readthedocs.io/)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Helm charts y ADR de orquestador

Deja la plataforma lista para Kubernetes si algún día lo necesita.

**Pasos:**
1. Charts de Helm de Pedidos e Inventario con probes y values por entorno.
2. Despliégalos en un cluster local con kind.
3. ADR-012: ECS vs. EKS para la plataforma.

**Terminado cuando:** helm install levanta ambos servicios en kind y ADR-012 escrito.

**Recursos:**
  - [Web: kind](https://kind.sigs.k8s.io/)

## S25 · Aprendizaje no supervisado · Analítica en AWS

**Objetivo:** Segmentar clientes sin etiquetas y consultar el data lake con servicios administrados.

**Conceptos clave:** K-means y RFM · Selección de k · PCA · Glue Data Catalog · Athena · Lake Formation

**Autoevaluación:**
1. ¿Cómo eliges k en k-means?
2. ¿Qué cobra Athena y cómo lo reduces?
3. ¿Para qué sirve el Glue Data Catalog?

### Lunes · Teoría · DAT-521 · Hands-On ML, caps. 8 y 9

Reducción de dimensionalidad y aprendizaje no supervisado, con el curso 3 de Ng como apoyo.

**Pasos:**
1. Reducción de dimensionalidad y PCA (40 min).
2. Clustering y k-means (50 min).
3. Ng: clustering y detección de anomalías (30 min).

**Terminado cuando:** Explicas k-means paso a paso.

**Recursos:**
  - [O'Reilly: Hands-On Machine Learning Geron unsupervised](https://learning.oreilly.com/search/?q=Hands-On%20Machine%20Learning%20Geron%20unsupervised)
  - [Coursera: Machine Learning Specialization Unsupervised Learning](https://www.coursera.org/search?query=Machine%20Learning%20Specialization%20Unsupervised%20Learning)

### Miércoles · Teoría · CLD-512 · Analítica en AWS

Glue, Athena y Lake Formation.

**Pasos:**
1. Sección de datos y analítica del curso (50 min).
2. Documentación de Athena: particiones y formatos (40 min).
3. Lake Formation: permisos sobre el lake (30 min).

**Terminado cuando:** Sabes reducir costo en Athena con particiones y Parquet.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Amazon Athena](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: segmentación sobre el data lake

Combina analítica en AWS y clustering.

**Pasos:**
1. Bucket curated, Glue Catalog y tablas en Terraform.
2. Consulta RFM (recencia, frecuencia, monto) en Athena.
3. K-means sobre el resultado; elige k con silueta y codo.
4. Mide el costo de las consultas.

**Terminado cuando:** 4 a 6 segmentos calculados desde Athena.

**Recursos:**
  - [Web: Glue Data Catalog](https://docs.aws.amazon.com/glue/latest/dg/catalog-and-crawler.html)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Segmentos y data lake documentado

Convierte los segmentos en acciones.

**Pasos:**
1. Nombre, perfil y acción de negocio por segmento.
2. Documenta el data lake: zonas, particiones y permisos.
3. Actualiza el C4 con el lake.

**Terminado cuando:** Documento de segmentación y del lake.

## S26 · Series de tiempo · Streaming en AWS · Demo v1.3

**Objetivo:** Pronosticar la demanda y llevar los eventos al lake en tiempo casi real.

**Conceptos clave:** Tendencia y estacionalidad · Baselines de pronóstico · Validación en series de tiempo · Kinesis Data Streams y Firehose · MSK

**Autoevaluación:**
1. ¿Por qué no se usa validación cruzada aleatoria en series de tiempo?
2. ¿Qué es un baseline estacional ingenuo?
3. ¿Firehose o Data Streams para llevar eventos a S3?

### Lunes · Teoría · DAT-521 · Forecasting: Principles and Practice

Libro gratuito de Rob Hyndman, la referencia en pronósticos.

**Pasos:**
1. Gráficas de series de tiempo y descomposición (40 min).
2. Métodos simples de pronóstico (40 min).
3. Evaluación de la precisión del pronóstico (40 min).

**Terminado cuando:** Explicas por qué un baseline simple es obligatorio.

**Recursos:**
  - [Web: Forecasting: Principles and Practice](https://otexts.com/fpp3/)

### Miércoles · Teoría · CLD-512 · Streaming en AWS

Kinesis y MSK.

**Pasos:**
1. Sección de Kinesis del curso (50 min).
2. Documentación de Firehose hacia S3 (30 min).
3. MSK: cuándo conviene sobre Kinesis (40 min).

**Terminado cuando:** Sabes cuándo usar cada servicio de streaming.

**Recursos:**
  - [Udemy: Ultimate AWS Certified Solutions Architect Associate Maarek](https://www.udemy.com/courses/search/?q=Ultimate%20AWS%20Certified%20Solutions%20Architect%20Associate%20Maarek)
  - [Web: Amazon Data Firehose](https://docs.aws.amazon.com/firehose/latest/dev/what-is-this-service.html)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: eventos al lake y baseline de demanda

Streaming de eventos y primer pronóstico.

**Pasos:**
1. Regla de EventBridge hacia Firehose y S3 en Parquet, en Terraform.
2. Ventas diarias por producto desde el modelo dbt.
3. Baseline estacional ingenuo y uno de suavizamiento exponencial con statsmodels.
4. MAE y MAPE en un periodo de prueba.

**Terminado cuando:** Eventos llegando al lake y baseline evaluado.

**Recursos:**
  - [Web: statsmodels: series de tiempo](https://www.statsmodels.org/stable/tsa.html)

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Pronóstico documentado y Demo v1.3

Muestra la plataforma con datos fluyendo.

**Pasos:**
1. Documento del baseline de demanda.
2. Demo v1.3 (3 min): streaming, data lake, segmentos y pronóstico.

**Terminado cuando:** Documento y video.

## S27 · Competencia Kaggle · GitOps y despliegues avanzados

**Objetivo:** Probar tus habilidades de ML frente a otros y desplegar sin miedo.

**Conceptos clave:** Kaggle Playground · Ensembles simples · Blue/green con CodeDeploy · Rollback automático · GitOps

**Autoevaluación:**
1. ¿Qué hicieron distinto los mejores notebooks públicos?
2. ¿Qué alarma usarías para revertir un despliegue?
3. ¿Qué ventaja da GitOps?

### Lunes · Teoría · DAT-521 · Kaggle Playground: análisis y baseline

Elige una competencia Playground activa de datos tabulares.

**Pasos:**
1. Lee la descripción y la métrica (15 min).
2. EDA rápido (45 min).
3. Baseline con validación cruzada y primer envío (60 min).

**Terminado cuando:** Primer envío con puntaje.

**Recursos:**
  - [Web: Competencias Playground](https://www.kaggle.com/competitions?hostSegmentIdFilter=8)

### Miércoles · Teoría · CLD-512 · Despliegues avanzados y GitOps

Blue/green, canary y GitOps.

**Pasos:**
1. Blue/green de ECS con CodeDeploy (50 min).
2. Rollback automático por alarmas (30 min).
3. Introducción a GitOps con Argo CD (40 min).

**Terminado cuando:** Sabes configurar un rollback por alarma.

**Recursos:**
  - [Web: Blue/green en ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/deployment-type-bluegreen.html)
  - [Web: Argo CD](https://argo-cd.readthedocs.io/)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: Kaggle, mejora y envío final

Itera con método.

**Pasos:**
1. 3 ideas de features nuevas.
2. Un segundo modelo y un ensemble simple.
3. Revisa 2 notebooks destacados y anota qué hicieron distinto.
4. Envío final.

**Terminado cuando:** Mejoraste tu puntaje y anotaste lo aprendido.

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Blue/green con rollback automático

Despliegues seguros para Pedidos.

**Pasos:**
1. Blue/green con CodeDeploy en Terraform.
2. Alarma de errores 5xx que dispara rollback.
3. Prueba: despliega una versión rota y verifica que vuelve sola.

**Terminado cuando:** La versión rota se revierte sin intervención.

## S28 · Comunicación de datos · FinOps

**Objetivo:** Contar historias con datos y controlar lo que cuesta la plataforma.

**Conceptos clave:** Storytelling con datos · Dashboards · Etiquetado de costos · Unit economics · Optimización de costos

**Autoevaluación:**
1. ¿Qué hace que un gráfico se entienda en 5 segundos?
2. ¿Cuánto cuesta procesar un pedido en tu plataforma?
3. Nombra 3 optimizaciones que aplicarías.

### Lunes · Teoría · DAT-521 · Storytelling with Data

Cómo comunicar con datos, de Cole Nussbaumer Knaflic.

**Pasos:**
1. Contexto y elección del gráfico (40 min).
2. Eliminar el desorden y enfocar la atención (40 min).
3. Documentación de Streamlit (40 min).

**Terminado cuando:** Rediseñaste 2 gráficos de tus notebooks.

**Recursos:**
  - [O'Reilly: Storytelling with Data](https://learning.oreilly.com/search/?q=Storytelling%20with%20Data)
  - [Web: Streamlit](https://docs.streamlit.io/)

### Miércoles · Teoría · CLD-512 · Cloud FinOps

Prácticas de FinOps aplicadas a la plataforma.

**Pasos:**
1. Cloud FinOps: fases informar, optimizar y operar (60 min).
2. Etiquetado y asignación de costos en AWS (30 min).
3. Costo por unidad: costo por pedido (30 min).

**Terminado cuando:** Defines la métrica costo por pedido.

**Recursos:**
  - [O'Reilly: Cloud FinOps](https://learning.oreilly.com/search/?q=Cloud%20FinOps)
  - [Web: Etiquetas de asignación de costos](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Lab: dashboard desplegado

Dashboard de negocio sobre los datos curados, desplegado con el pipeline.

**Pasos:**
1. Streamlit con ventas, cancelaciones, segmentos y pronóstico.
2. Lee desde Athena o desde extractos en S3.
3. Despliegue en ECS con el pipeline existente.
4. Protégelo con autenticación.

**Terminado cuando:** Dashboard accesible en AWS.

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Reporte de costos

Mide y reduce lo que cuesta la plataforma.

**Pasos:**
1. Etiquetas en todos los recursos.
2. Reporte de Cost Explorer por servicio y costo por pedido.
3. Aplica 3 optimizaciones y mide el ahorro.

**Terminado cuando:** Reporte con ahorro medido.

**Recursos:**
  - [Web: Cost Explorer](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html)

## S29 · Final del semestre 2 · Final

**Objetivo:** Cerrar el semestre con exámenes prácticos y la entrega de la plataforma v2.0.

**Conceptos clave:** ML cronometrado · Game day · Informe ejecutivo

**Autoevaluación:**
1. ¿Qué modelo pondrías en producción y por qué?
2. ¿Cuánto tardas en recrear todo desde cero?

### Lunes · Examen · DAT-521 · Final DAT-521: ML cronometrado

Ejercicio de 2 horas con un dataset tabular nuevo.

**Pasos:**
1. Exploración y features (40 min).
2. Modelo con validación honesta (50 min).
3. Informe con métricas y recomendación (30 min).

**Terminado cuando:** Modelo validado y conclusión clara.

**Recursos:**
  - [Web: Datasets de Kaggle](https://www.kaggle.com/datasets)

### Miércoles · Examen práctico · CLD-512 · Final CLD-512: game day

Prueba de operación real.

**Pasos:**
1. terraform destroy y recreación cronometrada con el pipeline.
2. Pide a alguien (o usa AWS FIS) que inyecte una falla sin decirte cuál.
3. Diagnostica y resuelve con el runbook.

**Terminado cuando:** Plataforma recreada y falla resuelta con el runbook.

**Recursos:**
  - [Web: AWS Fault Injection Service](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html)

### Viernes · Laboratorio integrado · DAT-521 + CLD-512 · Informe ejecutivo

El documento que leería un gerente.

**Pasos:**
1. 2 páginas: hallazgos, modelos, recomendaciones y costos.
2. Sin jerga innecesaria.
3. Revisión con la rúbrica de comunicación.

**Terminado cuando:** Informe de 2 páginas.

### Sábado · Proyecto integrador · DAT-521 + CLD-512 · Entrega del proyecto integrador v2.0

Entrega la plataforma con datos. Revisa requisitos y rúbrica en Proyecto integrador.

**Pasos:**
1. Completa los requisitos pendientes.
2. Video de destruir y recrear.
3. Autoevalúate con la rúbrica.
4. Etiqueta v2.0 y retro del semestre.

**Terminado cuando:** Etiqueta v2.0 y rúbrica con 75 puntos o más.

---

# SEM 3 · IA en producción (semanas 30 a 43)

Aprendes cómo funcionan los modelos y, en paralelo, cómo se diseñan y operan los sistemas que los usan. La plataforma gana predicción de demanda, un asistente RAG y un agente.

**Materias:** IA-531 Inteligencia Artificial: de Deep Learning a LLMs · ARQ-532 Arquitectura de Sistemas de IA y MLOps

**Hitos:** S34 Demo v2.1 · S36 Parcial · S38 Demo v2.2 · S42 Demo v2.3 · S43 Final y entrega v3.0

## S30 · Redes neuronales · Sistemas de ML en producción

**Objetivo:** Entender cómo aprende una red neuronal y en qué se diferencia un sistema de ML de un software tradicional.

**Conceptos clave:** MLP y activaciones · Backpropagation · Optimizadores · Requisitos de sistemas de ML · Datos como dependencia

**Autoevaluación:**
1. ¿Por qué sin activaciones no lineales una red profunda equivale a una lineal?
2. ¿Qué calcula backpropagation?
3. ¿Qué hace distinto a un sistema de ML?

### Lunes · Teoría · IA-531 · Hands-On ML, caps. 10 y 11

Redes neuronales artificiales y entrenamiento de redes profundas.

**Pasos:**
1. Del perceptrón al MLP (60 min).
2. Inicialización, activaciones, normalización y optimizadores (60 min).

**Terminado cuando:** Dibujas el grafo de una red de 2 capas y su gradiente.

**Recursos:**
  - [O'Reilly: Hands-On Machine Learning Geron neural networks](https://learning.oreilly.com/search/?q=Hands-On%20Machine%20Learning%20Geron%20neural%20networks)

### Miércoles · Teoría · ARQ-532 · Designing Machine Learning Systems, caps. 1 y 2

Chip Huyen sobre cómo se diseñan los sistemas de ML.

**Pasos:**
1. Panorama de los sistemas de ML (50 min).
2. Introducción al diseño de sistemas de ML: requisitos y proceso (50 min).
3. Requisitos de ML para la plataforma (20 min).

**Terminado cuando:** Lista de requisitos de ML para predicción de demanda y asistente.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: tu propio micrograd

Sigue el video de Karpathy programando a la par y luego entrena una red.

**Pasos:**
1. Video de micrograd programando a la par (puede tomar más de 2 h; termina el domingo si hace falta).
2. Clases Value, Neuron, Layer y MLP.
3. Entrena sobre el dataset moons y grafica la frontera.
4. Verifica tus gradientes contra PyTorch.

**Terminado cuando:** Accuracy superior a 95% y gradientes iguales a PyTorch.

**Recursos:**
  - [Web: Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html)
  - [Web: micrograd](https://github.com/karpathy/micrograd)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Hoja de ruta de IA de la plataforma

Planifica el semestre del proyecto.

**Pasos:**
1. ADR-013: capacidades de IA (demanda, asistente, agente) y su orden.
2. C4 con los servicios de IA planeados.
3. README de micrograd que explica backpropagation.

**Terminado cuando:** ADR-013, C4 y README.

## S31 · PyTorch · Datos para ML

**Objetivo:** Entrenar modelos con PyTorch sobre features bien construidas.

**Conceptos clave:** Tensores y autograd · Dataset y DataLoader · Ciclo de entrenamiento · Datos de entrenamiento y etiquetado · Feature engineering y feature stores

**Autoevaluación:**
1. ¿Qué hace optimizer.zero_grad?
2. ¿Qué es training-serving skew?
3. ¿Cuándo vale la pena un feature store?

### Lunes · Teoría · IA-531 · PyTorch: Learn the Basics

Tutoriales oficiales de PyTorch.

**Pasos:**
1. Tensores, datasets y DataLoaders (40 min).
2. Modelo y autograd (40 min).
3. Optimización y guardado (40 min).

**Terminado cuando:** Tutoriales ejecutados en Colab.

**Recursos:**
  - [Web: PyTorch: Learn the Basics](https://pytorch.org/tutorials/beginner/basics/intro.html)

### Miércoles · Teoría · ARQ-532 · Designing ML Systems, caps. 3 a 5

Ingeniería de datos para ML, datos de entrenamiento y features.

**Pasos:**
1. Fundamentos de ingeniería de datos para ML (40 min).
2. Datos de entrenamiento (40 min).
3. Feature engineering y training-serving skew (40 min).

**Terminado cuando:** Explicas training-serving skew con un ejemplo de la plataforma.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: features de demanda y modelo PyTorch

Construye features reproducibles desde el lake y entrena un modelo.

**Pasos:**
1. Job reproducible que calcula features de demanda desde el lake (rezagos, calendario, categoría).
2. Las mismas funciones sirven para entrenamiento e inferencia.
3. MLP en PyTorch con embedding de categoría y early stopping.
4. MAE y MAPE contra el baseline del semestre 2.

**Terminado cuando:** Modelo evaluado contra el baseline.

**Recursos:**
  - [Web: Google Colab](https://colab.research.google.com/)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Servicio de demanda v0 (batch)

Primera pieza de IA de la plataforma.

**Pasos:**
1. Job diario que genera predicciones de demanda y las escribe al lake.
2. Programado con el orquestador del semestre 2.
3. Predicciones visibles en el dashboard.

**Terminado cuando:** Predicciones diarias en el dashboard.

## S32 · Transformers y embeddings · Seguimiento de experimentos

**Objetivo:** Entender la arquitectura detrás de los LLMs y registrar experimentos de forma profesional.

**Conceptos clave:** Tokenización y embeddings · Atención · Encoder vs. decoder · Experiment tracking · Model registry · Evaluación offline

**Autoevaluación:**
1. ¿Qué problema de las RNN resuelve la atención?
2. ¿Diferencia entre BERT y GPT?
3. ¿Qué debe registrarse de cada experimento?

### Lunes · Teoría · IA-531 · Hands-On Large Language Models, caps. 1 a 3

Libro visual de Alammar y Grootendorst. Si queda tiempo en la semana, el video Let's build GPT de Karpathy.

**Pasos:**
1. Introducción a los modelos de lenguaje (35 min).
2. Tokens y embeddings (40 min).
3. Cómo funciona un transformer (45 min).

**Terminado cuando:** Explicas la atención con query, key y value.

**Recursos:**
  - [O'Reilly: Hands-On Large Language Models](https://learning.oreilly.com/search/?q=Hands-On%20Large%20Language%20Models)
  - [Web: The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
  - [YouTube: Karpathy Let's build GPT from scratch](https://www.youtube.com/results?search_query=Karpathy%20Let's%20build%20GPT%20from%20scratch)

### Miércoles · Teoría · ARQ-532 · MLflow y evaluación offline

Seguimiento de experimentos y registro de modelos.

**Pasos:**
1. MLflow: tracking, artefactos y model registry (60 min).
2. Designing ML Systems, cap. 6: desarrollo y evaluación offline (60 min).

**Terminado cuando:** Registraste un experimento de prueba.

**Recursos:**
  - [Web: MLflow](https://mlflow.org/docs/latest/)
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: Hugging Face y MLflow

Modelos preentrenados de NLP con seguimiento de experimentos.

**Pasos:**
1. Curso de Hugging Face, capítulos 1 a 3 (rápido).
2. Genera 500 reseñas sintéticas con etiqueta de sentimiento.
3. Clasifícalas con un modelo preentrenado y registra métricas en MLflow.
4. Embeddings con sentence-transformers y búsqueda de reseñas similares.

**Terminado cuando:** Clasificador evaluado y registrado en MLflow.

**Recursos:**
  - [Web: Curso de Hugging Face](https://huggingface.co/learn/llm-course)
  - [Web: Sentence Transformers](https://sbert.net/)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Comparativa de demanda en MLflow

Elige el modelo de demanda con evidencia.

**Pasos:**
1. Registra PyTorch, XGBoost y el baseline en MLflow.
2. Compara MAE, MAPE, tiempo de entrenamiento e inferencia.
3. Registra el mejor en el model registry.

**Terminado cuando:** Modelo en el registry con la comparativa.

## S33 · LLMs aplicados · Arquitectura de aplicaciones LLM

**Objetivo:** Integrar LLMs en un backend de forma confiable, con una arquitectura que se pueda operar.

**Conceptos clave:** Selección de modelo · Prompt engineering · Salidas estructuradas · Gateway de modelos · Caché y guardrails · Costo por solicitud

**Autoevaluación:**
1. ¿Por qué validar la salida del LLM con un esquema?
2. ¿Qué responsabilidades tiene un gateway de modelos?
3. ¿Cómo estimas el costo mensual de un endpoint con LLM?

### Lunes · Teoría · IA-531 · AI Engineering, caps. 1 a 5

Chip Huyen sobre aplicaciones con modelos fundacionales.

**Pasos:**
1. Introducción a la ingeniería de IA (25 min).
2. Modelos fundacionales (35 min).
3. Metodología de evaluación (30 min).
4. Prompt engineering (30 min).

**Terminado cuando:** Explicas cuándo usar prompting, RAG o fine-tuning.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen)

### Miércoles · Teoría · ARQ-532 · Arquitectura de una aplicación LLM

El capítulo de arquitectura de AI Engineering y cursos cortos de function calling.

**Pasos:**
1. AI Engineering: arquitectura de ingeniería de IA (gateway, caché, guardrails) (60 min).
2. Curso corto de function calling o tool use (40 min).
3. Diagrama de la arquitectura LLM de la plataforma (20 min).

**Terminado cuando:** Diagrama con gateway, caché, guardrails y observabilidad.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen architecture](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20architecture)
  - [Web: Cursos cortos de DeepLearning.AI](https://www.deeplearning.ai/short-courses/)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: servicio LLM detrás de un gateway

Construye la capa que usarán todas las funciones de IA.

**Pasos:**
1. Servicio FastAPI que llama a un proveedor de LLM a través de un módulo gateway propio.
2. Salida estructurada validada con Pydantic.
3. Timeouts, reintentos, fallback a otro modelo.
4. Registro de tokens, latencia y costo por solicitud; llave en Secrets Manager.

**Terminado cuando:** JSON válido siempre y costo registrado por solicitud.

**Recursos:**
  - [Web: FastAPI](https://fastapi.tiangolo.com/)
  - [Web: Pydantic](https://docs.pydantic.dev/)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Endpoint /resumen-pedido

Primera función LLM de la plataforma.

**Pasos:**
1. Endpoint que resume el historial de un pedido para soporte.
2. Tests unitarios con el LLM simulado.
3. 10 casos de evaluación con salida esperada.
4. ADR-014: modelo y proveedor.

**Terminado cuando:** Endpoint con tests y ADR-014.

## S34 · RAG · Infraestructura de recuperación · Demo v2.1

**Objetivo:** Responder sobre información propia citando fuentes, con la infraestructura adecuada.

**Conceptos clave:** Chunking · Búsqueda híbrida · Reranking · Citas y grounding · pgvector, OpenSearch, Bedrock Knowledge Bases

**Autoevaluación:**
1. ¿Qué pasa si los chunks son muy grandes o muy pequeños?
2. ¿Por qué la búsqueda híbrida suele ganar?
3. ¿Cuándo elegirías un servicio administrado de RAG?

### Lunes · Teoría · IA-531 · RAG en AI Engineering y Hands-On LLMs

Teoría y práctica de Retrieval-Augmented Generation.

**Pasos:**
1. AI Engineering: RAG (50 min).
2. Hands-On LLMs: búsqueda semántica y generación aumentada (50 min).
3. Decisiones de diseño de un RAG (20 min).

**Terminado cuando:** 6 decisiones de diseño con sus opciones.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen RAG](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20RAG)
  - [O'Reilly: Hands-On Large Language Models](https://learning.oreilly.com/search/?q=Hands-On%20Large%20Language%20Models)

### Miércoles · Teoría · ARQ-532 · Opciones de infraestructura vectorial

Compara dónde vivirán los vectores.

**Pasos:**
1. pgvector en RDS: índices HNSW e IVFFlat (40 min).
2. OpenSearch con búsqueda vectorial (30 min).
3. Bedrock Knowledge Bases (30 min).
4. Tabla comparativa: costo, operación, latencia (20 min).

**Terminado cuando:** Tabla comparativa lista.

**Recursos:**
  - [Web: pgvector](https://github.com/pgvector/pgvector)
  - [Web: Bedrock Knowledge Bases](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: recuperación con pgvector

Construye la recuperación del asistente de soporte.

**Pasos:**
1. Escribe 20 documentos de políticas y FAQs (envíos, devoluciones, pagos).
2. Chunking por secciones con superposición.
3. Embeddings en pgvector sobre el RDS existente.
4. Búsqueda híbrida con texto completo de Postgres y reranking.

**Terminado cuando:** El documento correcto aparece en el top 5 para 10 preguntas de prueba.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Asistente con citas y Demo v2.1

Completa el asistente.

**Pasos:**
1. Endpoint /soporte/preguntar con respuesta y fuentes.
2. Responde que no sabe cuando no hay contexto.
3. ADR-015: infraestructura vectorial.
4. Demo v2.1 (3 min): resumen de pedido y asistente.

**Terminado cuando:** El asistente cita fuentes y no inventa; video listo.

## S35 · Agentes y MCP · Serving de modelos

**Objetivo:** Construir agentes que usan las APIs de la plataforma y servir modelos de forma eficiente.

**Conceptos clave:** Workflows vs. agentes · Tool use · Model Context Protocol · Confirmación humana · Predicción online vs. batch · SageMaker y Bedrock

**Autoevaluación:**
1. ¿Cuándo un workflow fijo es mejor que un agente?
2. ¿Qué acciones requieren confirmación humana?
3. ¿Cuándo sirves un modelo online en vez de batch?

### Lunes · Teoría · IA-531 · Agentes y MCP

Diseño de agentes y el protocolo MCP.

**Pasos:**
1. AI Engineering: agentes (50 min).
2. Building effective agents de Anthropic (30 min).
3. Conceptos de MCP: servidores, herramientas y recursos (40 min).

**Terminado cuando:** Describes 3 patrones de workflow y cuándo pasar a un agente.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen agents](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20agents)
  - [Web: Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
  - [Web: Model Context Protocol](https://modelcontextprotocol.io/)

### Miércoles · Teoría · ARQ-532 · Designing ML Systems, cap. 7: despliegue

Servir modelos en producción.

**Pasos:**
1. Despliegue y servicio de predicciones (60 min).
2. SageMaker endpoints vs. contenedor propio en ECS (30 min).
3. Bedrock como modelo administrado (30 min).

**Terminado cuando:** Decides cómo servir el modelo de demanda.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)
  - [Web: Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
  - [Web: Amazon Bedrock](https://docs.aws.amazon.com/bedrock/)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: servidor MCP y agente

Expón la plataforma como herramientas para un agente.

**Pasos:**
1. Servidor MCP con consultar_pedido, estado_envio y cancelar_pedido.
2. Validación de entradas y autorización por cliente.
3. cancelar_pedido pide confirmación explícita.
4. Agente desplegado en ECS que resuelve: ¿dónde está mi pedido y puedo cancelarlo?

**Terminado cuando:** El agente responde y pide confirmación antes de cancelar.

**Recursos:**
  - [Web: MCP: construir un servidor](https://modelcontextprotocol.io/docs/develop/build-server)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Agente con guardrails y trazas

Seguridad y visibilidad del agente.

**Pasos:**
1. Límite de pasos y de costo por conversación.
2. Herramientas permitidas por rol.
3. Trazas de cada paso del agente.
4. ADR-016: workflow vs. agente para soporte.

**Terminado cuando:** Ves en las trazas cada herramienta usada y ADR-016.

**Recursos:**
  - [Web: Langfuse](https://langfuse.com/docs)

## S36 · Parcial de mitad de semestre · Parcial

**Objetivo:** Medir el avance en IA y en arquitectura de sistemas de IA.

**Conceptos clave:** Conceptos de deep learning y LLMs · System design con LLM · Revisión de arquitectura

**Autoevaluación:**
1. ¿Qué parte del sistema de IA es la más frágil?
2. ¿Qué concepto te costó más explicar?

### Lunes · Examen · IA-531 · Parcial IA-531

Parte escrita y parte práctica, sin consultar.

**Pasos:**
1. Explica por escrito backpropagation, atención y RAG (50 min).
2. Práctica: implementa recuperación sobre 10 documentos nuevos y mide recall@5 (60 min).
3. Autocalificación (10 min).

**Terminado cuando:** Explicaciones correctas y recall@5 de 0,8 o más.

### Miércoles · Examen · ARQ-532 · Parcial ARQ-532: system design con LLM

Diseña un asistente con LLM para 10.000 usuarios diarios.

**Pasos:**
1. Requisitos, estimación de tokens y costo (20 min).
2. Arquitectura: gateway, RAG, caché, guardrails, observabilidad (40 min).
3. Trade-offs y riesgos (20 min).
4. Autocalificación (40 min con revisión del diseño).

**Terminado cuando:** Diseño completo con costo estimado.

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Revisión de la arquitectura de IA

Usa AI Engineering como checklist.

**Pasos:**
1. Marca qué componentes tienes y cuáles faltan.
2. Agrega los riesgos de IA a la matriz de riesgos.
3. Lista de deuda técnica de IA.

**Terminado cuando:** Checklist y matriz actualizadas.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Estabilización y retro de mitad de semestre

Paga deuda antes de seguir.

**Pasos:**
1. Cierra pendientes y actualiza diagramas.
2. Revisa ADR-013 a ADR-016.
3. Retro de mitad de semestre.

**Terminado cuando:** Repositorio al día y retro escrita.

## S37 · Evaluación de LLMs · Observabilidad de LLMs

**Objetivo:** Medir la calidad de los sistemas con LLM y ver lo que pasa en producción.

**Conceptos clave:** Golden sets · Fidelidad y relevancia · LLM como juez · Evals en CI · Trazas de LLM · Tokens y costo por traza

**Autoevaluación:**
1. ¿Qué sesgos tiene un LLM usado como juez?
2. ¿Cómo evitas que un cambio de prompt degrade la calidad sin notarlo?
3. ¿Qué datos de una traza de LLM son sensibles?

### Lunes · Teoría · IA-531 · Evaluación en AI Engineering

Capítulos de evaluación de modelos y sistemas.

**Pasos:**
1. Evaluación de modelos fundacionales (60 min).
2. Evaluación de sistemas de IA (60 min).

**Terminado cuando:** Diseñas la estrategia de evaluación del asistente.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen evaluation](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20evaluation)
  - [Web: Cursos cortos de DeepLearning.AI](https://www.deeplearning.ai/short-courses/)

### Miércoles · Teoría · ARQ-532 · Observabilidad de LLMs

Trazas, métricas y costos de aplicaciones con LLM.

**Pasos:**
1. Documentación de Langfuse: trazas, sesiones y evaluaciones (50 min).
2. Convenciones semánticas de OpenTelemetry para IA generativa (30 min).
3. Qué datos ocultar en las trazas (20 min).
4. Herramienta de evals: promptfoo, Ragas o DeepEval (20 min).

**Terminado cuando:** Elegiste herramienta de evals y de trazas.

**Recursos:**
  - [Web: Langfuse](https://langfuse.com/docs)
  - [Web: OpenTelemetry GenAI](https://opentelemetry.io/docs/specs/semconv/gen-ai/)
  - [Web: promptfoo](https://www.promptfoo.dev/docs/intro/)
  - [Web: Ragas](https://docs.ragas.io/)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: suite de evals y trazas

Mide el asistente y el agente.

**Pasos:**
1. Golden set de 30 preguntas con respuesta y fuente esperadas.
2. Métricas de fidelidad, relevancia y recuperación.
3. LLM como juez con rúbrica; valida 10 casos a mano.
4. Trazas de todas las llamadas con tokens y costo.

**Terminado cuando:** Métricas calculadas y trazas visibles.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Gate de calidad en CI

Ningún cambio baja la calidad sin que lo sepas.

**Pasos:**
1. Evals en el pipeline con umbral mínimo.
2. Prueba: un prompt peor bloquea el despliegue.
3. Reporte de calidad con ejemplos de fallas.

**Terminado cuando:** El pipeline bloquea un cambio que empeora la calidad.

## S38 · Fine-tuning · Monitoreo y drift · Demo v2.2

**Objetivo:** Saber cuándo ajustar un modelo y detectar cuándo un modelo en producción se degrada.

**Conceptos clave:** Fine-tuning completo vs. PEFT · LoRA · Data drift vs. concept drift · Métricas de monitoreo · Alertas de modelos

**Autoevaluación:**
1. ¿Cuándo vale la pena hacer fine-tuning en vez de RAG?
2. ¿Diferencia entre data drift y concept drift?
3. ¿Qué monitoreas en un modelo de demanda?

### Lunes · Teoría · IA-531 · Fine-tuning y PEFT

El capítulo de fine-tuning de AI Engineering y la documentación de PEFT.

**Pasos:**
1. AI Engineering: fine-tuning (60 min).
2. Hugging Face PEFT y LoRA (40 min).
3. Cuándo no hacer fine-tuning (20 min).

**Terminado cuando:** Criterios escritos para decidir fine-tuning.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen finetuning](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20finetuning)
  - [Web: PEFT](https://huggingface.co/docs/peft)

### Miércoles · Teoría · ARQ-532 · Designing ML Systems, cap. 8: drift y monitoreo

Cambios de distribución y monitoreo de modelos.

**Pasos:**
1. Causas de fallas de modelos en producción (40 min).
2. Detección de cambios de distribución (40 min).
3. Monitoreo y observabilidad de ML (40 min).

**Terminado cuando:** Plan de monitoreo para el modelo de demanda.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)
  - [Web: Evidently](https://docs.evidentlyai.com/)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: LoRA y reporte de drift

Ajusta un modelo pequeño y monitorea el de demanda.

**Pasos:**
1. Fine-tune LoRA de un clasificador de reseñas en Colab.
2. Compáralo con el modelo sin ajustar en MLflow.
3. Reporte de Evidently: datos de entrenamiento vs. últimas 4 semanas.
4. Simula un cambio de comportamiento y verifica que se detecta.

**Terminado cuando:** Comparativa LoRA registrada y drift detectado.

**Recursos:**
  - [Web: Google Colab](https://colab.research.google.com/)

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Demanda en producción y Demo v2.2

El modelo de demanda queda operando.

**Pasos:**
1. Servicio de predicción online en ECS o SageMaker, cargando desde el registry.
2. Reporte de drift semanal y alarma.
3. Demo v2.2 (3 min): evals, trazas, drift y modelo en producción.

**Terminado cuando:** Endpoint en producción con alarma y video.

## S39 · Seguridad de LLMs · Aprendizaje continuo

**Objetivo:** Defender la plataforma de ataques a sistemas con LLM y automatizar el ciclo de vida de los modelos.

**Conceptos clave:** Prompt injection directa e indirecta · Exfiltración por herramientas · OWASP Top 10 para LLM · Reentrenamiento · CI/CD para ML

**Autoevaluación:**
1. ¿Qué es prompt injection indirecta?
2. ¿Cómo limitarías el daño si el agente es manipulado?
3. ¿Cada cuánto reentrenarías el modelo de demanda y por qué?

### Lunes · Teoría · IA-531 · Seguridad de aplicaciones LLM

Amenazas específicas de los sistemas con LLM.

**Pasos:**
1. OWASP Top 10 para LLM (50 min).
2. Artículos de Simon Willison sobre prompt injection (40 min).
3. Modelo de amenazas del asistente y del agente (30 min).

**Terminado cuando:** Lista de 6 ataques con su mitigación.

**Recursos:**
  - [Web: OWASP Top 10 para LLM](https://genai.owasp.org/llm-top-10/)
  - [Web: Simon Willison: prompt injection](https://simonwillison.net/tags/prompt-injection/)

### Miércoles · Teoría · ARQ-532 · Designing ML Systems, cap. 9: aprendizaje continuo

Reentrenamiento y pruebas en producción.

**Pasos:**
1. Aprendizaje continuo (50 min).
2. Pruebas en producción: shadow, A/B, canary (40 min).
3. Pipelines de ML en GitHub Actions o SageMaker Pipelines (30 min).

**Terminado cuando:** Defines la política de reentrenamiento.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: red teaming de la plataforma

Ataca tu propio asistente y agente.

**Pasos:**
1. Instrucciones escondidas en un documento del RAG.
2. Intentos de que el agente cancele pedidos ajenos.
3. Intentos de extraer el prompt del sistema o datos de otros clientes.
4. Aplica guardrails y repite las pruebas.

**Terminado cuando:** Ataques documentados y bloqueados tras las mitigaciones.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Pipeline de reentrenamiento

El modelo de demanda se mantiene solo.

**Pasos:**
1. Pipeline: reentrenar → evaluar → registrar → desplegar solo si mejora.
2. Despliegue en modo shadow antes de promover.
3. Reporte de seguridad del red teaming.

**Terminado cuando:** Pipeline funcionando y reporte de seguridad.

## S40 · Modelos abiertos · Costos y optimización de inferencia

**Objetivo:** Comparar modelos abiertos con modelos por API y reducir costo y latencia.

**Conceptos clave:** Modelos abiertos y cuantización · Ollama y vLLM · Caché semántica · Enrutamiento de modelos · Batching y prompt caching

**Autoevaluación:**
1. ¿Qué pierdes al cuantizar un modelo?
2. ¿Cuándo un modelo local sale más barato que una API?
3. ¿Qué solicitudes enrutarías a un modelo pequeño?

### Lunes · Teoría · IA-531 · Modelos abiertos e inferencia local

Ecosistema de modelos abiertos y cómo servirlos.

**Pasos:**
1. Hugging Face: modelos abiertos y licencias (30 min).
2. Cuantización y formatos (40 min).
3. Documentación de Ollama y vLLM (50 min).

**Terminado cuando:** Sabes elegir un modelo abierto por tamaño, licencia y tarea.

**Recursos:**
  - [Web: Ollama](https://ollama.com/)
  - [Web: vLLM](https://docs.vllm.ai/)
  - [Web: Hugging Face Models](https://huggingface.co/models)

### Miércoles · Teoría · ARQ-532 · Optimización de inferencia

El capítulo de optimización de inferencia de AI Engineering.

**Pasos:**
1. AI Engineering: optimización de inferencia (60 min).
2. Caché semántica y prompt caching (30 min).
3. Enrutamiento por complejidad de la solicitud (30 min).

**Terminado cuando:** Plan de optimización para el asistente.

**Recursos:**
  - [O'Reilly: AI Engineering Chip Huyen inference optimization](https://learning.oreilly.com/search/?q=AI%20Engineering%20Chip%20Huyen%20inference%20optimization)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: modelo abierto vs. API

Compara con datos en vez de opiniones.

**Pasos:**
1. Sirve un modelo abierto con Ollama en local.
2. Corre el golden set con el modelo abierto y con la API.
3. Compara calidad, latencia y costo por cada 1.000 solicitudes.
4. Agrega caché semántica y mide de nuevo.

**Terminado cuando:** Tabla comparativa con 3 configuraciones.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Enrutamiento y reporte de costos de IA

Optimiza el costo de IA de la plataforma.

**Pasos:**
1. Enrutador en el gateway: modelo pequeño para preguntas simples.
2. Reporte de costos de IA antes y después.
3. ADR-017: estrategia de modelos y enrutamiento.

**Terminado cuando:** Ahorro medido y ADR-017.

## S41 · Agentes avanzados · Plataforma de ML

**Objetivo:** Construir agentes con estado y entender la infraestructura que sostiene el ML de una empresa.

**Conceptos clave:** Memoria y estado · Planificación y flujos multi-paso · Human-in-the-loop · Plataforma de ML · Infraestructura y herramientas de MLOps

**Autoevaluación:**
1. ¿Qué riesgos trae la memoria de largo plazo en un agente?
2. ¿Qué componentes tiene una plataforma de ML?
3. ¿Construir o comprar la plataforma de ML?

### Lunes · Teoría · IA-531 · Agentes con estado

Memoria, planificación y control en agentes.

**Pasos:**
1. Documentación de LangGraph: estado, memoria y human-in-the-loop (60 min).
2. Curso corto de agentes en DeepLearning.AI (60 min).

**Terminado cuando:** Sabes modelar un agente como grafo de estados.

**Recursos:**
  - [Web: LangGraph](https://langchain-ai.github.io/langgraph/)
  - [Web: Cursos cortos de DeepLearning.AI](https://www.deeplearning.ai/short-courses/)

### Miércoles · Teoría · ARQ-532 · Designing ML Systems, cap. 10: infraestructura

Infraestructura y herramientas para MLOps.

**Pasos:**
1. Capas de infraestructura de ML (50 min).
2. Plataformas de ML: componentes (40 min).
3. Construir vs. comprar (30 min).

**Terminado cuando:** Mapa de la plataforma de ML actual con sus brechas.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: agente multi-paso con supervisión humana

Un agente que resuelve casos de soporte complejos.

**Pasos:**
1. Agente en LangGraph con memoria de la conversación.
2. Flujo: entender caso → consultar pedido → proponer solución → pedir aprobación → ejecutar.
3. Punto de aprobación humana antes de acciones con efecto.
4. Trazas de cada paso.

**Terminado cuando:** El agente resuelve un caso de 4 pasos con aprobación humana.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Pruebas de carga de los servicios de IA

Mide cómo responde la IA bajo carga.

**Pasos:**
1. k6 sobre /soporte/preguntar, /prediccion y el agente.
2. p95, tasa de error y costo por cada 1.000 solicitudes.
3. Ajusta concurrencia, timeouts y límites de tasa.

**Terminado cuando:** Tabla de capacidad y costo de los servicios de IA.

**Recursos:**
  - [Web: k6](https://k6.io/docs/)

## S42 · IA responsable · Gobierno de IA · Demo v2.3

**Objetivo:** Construir IA en la que el negocio y los usuarios puedan confiar.

**Conceptos clave:** Sesgo y equidad · Privacidad y datos personales · Model cards · Gestión de riesgos de IA · Trazabilidad de decisiones

**Autoevaluación:**
1. ¿Cómo detectarías sesgo en el modelo de cancelación?
2. ¿Qué datos personales llegan al LLM y cómo los proteges?
3. ¿Qué incluye una model card?

### Lunes · Teoría · IA-531 · Designing ML Systems, cap. 11: IA responsable

Responsabilidad, privacidad y sesgo.

**Pasos:**
1. IA responsable (60 min).
2. Privacidad y manejo de datos personales (30 min).
3. Casos reales de fallas de IA (30 min).

**Terminado cuando:** Lista de riesgos de IA responsable de la plataforma.

**Recursos:**
  - [O'Reilly: Designing Machine Learning Systems Chip Huyen](https://learning.oreilly.com/search/?q=Designing%20Machine%20Learning%20Systems%20Chip%20Huyen)

### Miércoles · Teoría · ARQ-532 · Gobierno de IA

Marcos para gestionar riesgos de IA.

**Pasos:**
1. NIST AI Risk Management Framework: funciones principales (50 min).
2. Model cards: estructura y ejemplos (30 min).
3. Política de uso de datos en IA para la plataforma (40 min).

**Terminado cuando:** Borrador de política de datos en IA.

**Recursos:**
  - [Web: NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework)
  - [Web: Model cards en Hugging Face](https://huggingface.co/docs/hub/model-cards)

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Lab: model cards, sesgo y PII

Aplica el gobierno sobre lo construido.

**Pasos:**
1. Model card del modelo de demanda y del asistente.
2. Mide el desempeño del modelo de cancelación por segmento de cliente.
3. Enmascara datos personales en prompts y trazas.
4. Prueba que ninguna traza guarda datos personales en claro.

**Terminado cuando:** Model cards, análisis por segmento y trazas sin PII.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Documento de arquitectura de IA y Demo v2.3

Documenta la IA de la plataforma.

**Pasos:**
1. Arquitectura de IA: C4, gateway, RAG, agente, MLOps, seguridad y gobierno.
2. Índice de ADRs de IA.
3. Demo v2.3 (3 min): agente, optimización de costos y gobierno.

**Terminado cuando:** Documento y video.

## S43 · Final del semestre 3 · Final

**Objetivo:** Cerrar el semestre con exámenes y la entrega de la plataforma v3.0.

**Conceptos clave:** Práctico de IA · System design de ML · Reporte de evaluación

**Autoevaluación:**
1. ¿Qué función de IA aporta más valor y por qué?
2. ¿Qué harías distinto si empezaras el semestre hoy?

### Lunes · Examen · IA-531 · Final IA-531: práctico

Ejercicio de 2 horas sin consultar tu código anterior.

**Pasos:**
1. Construye un RAG pequeño sobre 15 documentos nuevos (60 min).
2. Golden set de 10 preguntas y métricas (40 min).
3. Informe de resultados (20 min).

**Terminado cuando:** RAG funcionando con métricas reportadas.

### Miércoles · Examen · ARQ-532 · Final ARQ-532: system design de ML

Diseña un sistema de detección de fraude en pagos o de recomendaciones.

**Pasos:**
1. Requisitos, datos y features (25 min).
2. Entrenamiento, serving y monitoreo (35 min).
3. Trade-offs, costos y riesgos (20 min).
4. Autocalificación (40 min).

**Terminado cuando:** Diseño completo con plan de monitoreo.

### Viernes · Laboratorio integrado · IA-531 + ARQ-532 · Reporte de evaluación final

El reporte que entregarías a un comité.

**Pasos:**
1. Calidad, latencia, costo y seguridad de cada función de IA.
2. Comparativas clave (modelo abierto vs. API, LoRA).
3. Riesgos abiertos.

**Terminado cuando:** Reporte de 2 a 3 páginas.

### Sábado · Proyecto integrador · IA-531 + ARQ-532 · Entrega del proyecto integrador v3.0

Entrega la plataforma con IA. Revisa requisitos y rúbrica en Proyecto integrador.

**Pasos:**
1. Completa los requisitos pendientes.
2. Demo grabada de 5 minutos.
3. Autoevalúate con la rúbrica.
4. Etiqueta v3.0 y retro del semestre.

**Terminado cuando:** Etiqueta v3.0 y rúbrica con 75 puntos o más.

---

# CAPSTONE · Defensa final (semanas 44 a 46)

Como el proyecto ya está integrado, el capstone se dedica a pulir, documentar y defender la plataforma como lo haría un arquitecto frente a un comité técnico.

**Materias:** CAP-540 Proyecto Integrador Final

**Hitos:** S46 Defensa final

## S44 · Arquitectura integrada v2

**Objetivo:** Unificar los tres semestres en un solo documento coherente y probar la operación completa.

**Conceptos clave:** Documento de arquitectura v2 · Revisión de ADRs · Game day completo

**Autoevaluación:**
1. ¿Qué decisiones de distintos semestres entran en conflicto?
2. ¿Qué falla te preocupa más en producción?

### Lunes · Capstone · CAP-540 · C4 integrado

Diagramas del sistema completo.

**Pasos:**
1. Contexto con usuarios, operadores y sistemas externos.
2. Contenedores: servicios, datos, IA y nube.
3. Componentes del servicio más complejo.

**Terminado cuando:** C4 de 3 niveles del sistema completo.

**Recursos:**
  - [Web: Modelo C4](https://c4model.com/)

### Miércoles · Capstone · CAP-540 · Revisión de todos los ADRs

Coherencia de las decisiones.

**Pasos:**
1. Marca como reemplazados los que ya no aplican.
2. Escribe los que falten.
3. Índice de ADRs con estado.

**Terminado cuando:** Índice sin contradicciones.

### Viernes · Capstone · CAP-540 · Game day completo

Prueba de operación de todo el sistema.

**Pasos:**
1. Inyecta 3 fallas: base de datos, proveedor de LLM y cola de eventos.
2. Resuelve cada una con el runbook.
3. Actualiza el runbook con lo aprendido.

**Terminado cuando:** Las 3 fallas resueltas y runbook actualizado.

**Recursos:**
  - [Web: AWS Fault Injection Service](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html)

### Sábado · Capstone · CAP-540 · Documento de arquitectura v2

El documento que defenderás.

**Pasos:**
1. Integra los documentos de los 3 semestres.
2. Resumen ejecutivo de 1 página.
3. Etiqueta docs-v2.

**Terminado cuando:** Documento v2 publicado.

**Recursos:**
  - [Web: arc42](https://arc42.org/overview)

## S45 · Pulido y ensayo

**Objetivo:** Dejar el repositorio y la narrativa listos para presentar.

**Conceptos clave:** Guion de la demo · Repositorio ordenado · Artículo técnico

**Autoevaluación:**
1. ¿Cuál es la historia que quieres contar en 10 minutos?
2. ¿Qué decisión difícil merece un artículo?

### Lunes · Capstone · CAP-540 · Guion de la demo

Estructura la presentación.

**Pasos:**
1. Problema, arquitectura, demo, trade-offs, aprendizajes.
2. Elige 3 momentos de la demo que muestren criterio.
3. Tiempos por sección.

**Terminado cuando:** Guion de 10 minutos.

### Miércoles · Capstone · CAP-540 · Repositorio ordenado

Que cualquiera pueda entender y correr el proyecto.

**Pasos:**
1. README principal con arquitectura, cómo correrlo y enlaces.
2. Limpia ramas, archivos sueltos y secretos de prueba.
3. Badges de CI.

**Terminado cuando:** README que permite levantar todo siguiendo los pasos.

**Recursos:**
  - [Web: Cómo escribir un buen README](https://www.makeareadme.com/)

### Viernes · Capstone · CAP-540 · Borrador de la demo

Primera grabación.

**Pasos:**
1. Graba siguiendo el guion.
2. Mírala y anota qué cortar o mejorar.
3. Ajusta el guion.

**Terminado cuando:** Borrador grabado con notas de mejora.

### Sábado · Capstone · CAP-540 · Borrador del artículo técnico

Comparte una decisión difícil del proyecto.

**Pasos:**
1. Tema: una decisión con trade-offs reales.
2. 1.200 a 1.800 palabras con diagramas.
3. Pide revisión a un colega.

**Terminado cuando:** Borrador completo.

## S46 · Defensa final · Defensa

**Objetivo:** Defender tu trabajo, dejar evidencia pública y planear el siguiente paso.

**Conceptos clave:** Demo final · Artículo publicado · Retrospectiva

**Autoevaluación:**
1. ¿Qué harías distinto si empezaras hoy?
2. ¿Qué rol o proyecto buscas con estas habilidades?

### Lunes · Capstone · CAP-540 · Grabar la demo final

Versión final de 10 minutos.

**Pasos:**
1. Graba con el guion ajustado.
2. Edita y publícala en el README.

**Terminado cuando:** Video publicado.

### Miércoles · Capstone · CAP-540 · Publicar el artículo

Visibilidad profesional.

**Pasos:**
1. Incorpora la revisión del colega.
2. Publica en tu blog o LinkedIn.
3. Enlázalo desde el README.

**Terminado cuando:** Artículo publicado.

### Viernes · Capstone · CAP-540 · Retrospectiva de las 46 semanas

Mira hacia atrás con datos.

**Pasos:**
1. Revisa todo tu learning log.
2. Qué funcionó, qué no y qué cambió en tu trabajo.
3. Habilidades que subieron de nivel.

**Terminado cuando:** Retrospectiva de 1 a 2 páginas.

### Sábado · Capstone · CAP-540 · Presentación final

Cierre del plan. Revisa requisitos y rúbrica en Proyecto integrador.

**Pasos:**
1. Presentación de 12 a 15 diapositivas.
2. Autoevaluación con la rúbrica.
3. Plan de aprendizaje del próximo año.
4. Etiqueta v3.1-final.

**Terminado cuando:** Etiqueta v3.1-final y rúbrica con 75 puntos o más.
