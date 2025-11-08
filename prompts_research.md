# Estructura de investigación Patron Saga

## 🧩 1. Fundamentos del patrón Saga

**Prompt:**

> Explica de forma profunda y práctica el patrón Saga en sistemas distribuidos.
> Incluye las diferencias entre **coreografía y orquestación**, cómo maneja **transacciones distribuidas sin bloqueo**, y cómo funcionan las **acciones compensatorias**.
> Usa un ejemplo realista de flujo “pedido → pago → envío”, describiendo cada paso, posibles fallos y cómo se compensan.
> Agrega diagramas conceptuales y pseudo-código orientativo (por ejemplo, en Spring Boot o Node.js).

---

## ⚙️ 2. Transacciones distribuidas vs. Sagas

**Prompt:**

> Compara detalladamente **Two-Phase Commit (2PC)** y el **patrón Saga**.
> Explica las ventajas, desventajas y cuándo conviene usar uno u otro.
> Incluye cómo afectan la **latencia**, el **bloqueo de recursos** y la **disponibilidad**.
> Termina con un cuadro comparativo y un ejemplo de caso de uso donde migrarías de 2PC a Sagas para mejorar resiliencia.

---

## 🔀 3. Modelos de comunicación asíncrona y eventos

**Prompt:**

> Describe cómo la **arquitectura basada en eventos (Event-Driven Architecture)** soporta el patrón Saga.
> Explica los tipos de **brokers** (Kafka, RabbitMQ, Pub/Sub) y las **garantías de entrega** (“at least once”, “exactly once”).
> Profundiza en cómo implementar **idempotencia** y **manejo de mensajes duplicados** en microservicios que usan Sagas.
> Incluye ejemplos de diseño de colas, retries y mensajes de compensación.

---

## 🧱 4. Event Sourcing vs. Saga pattern

**Prompt:**

> Diferencia **Event Sourcing**, **Event-Driven Architecture** y **Saga pattern**.
> Explica qué problema resuelve cada uno, cuándo se complementan y cuándo no.
> Muestra cómo podrían coexistir en un mismo sistema (por ejemplo, usando Event Sourcing para persistencia y Sagas para orquestación).
> Incluye ejemplos visuales de flujos de eventos y almacenamiento de estados.

---

## 🧠 5. Consistencia eventual y compensación

**Prompt:**

> Explica el concepto de **consistencia eventual** en sistemas distribuidos y cómo el patrón Saga lo implementa mediante **transacciones compensatorias**.
> Describe estrategias comunes como **retry**, **timeouts**, **dead letter queues**, y cómo asegurar **idempotencia** en acciones compensatorias.
> Usa un ejemplo de error real (por ejemplo: “falló el envío tras el pago confirmado”) y muestra cómo el sistema se recupera con consistencia eventual.

---

## 🧩 6. Diseño de límites (Bounded Contexts / DDD)

**Prompt:**

> Explica cómo los **Bounded Contexts** del **Domain-Driven Design (DDD)** guían el diseño de sistemas distribuidos con el patrón Saga.
> Describe cómo definir correctamente los límites de datos y transacciones.
> Muestra ejemplos de **context mapping** y cómo Sagas se encargan de coordinar operaciones entre distintos contextos.
> Incluye un ejemplo de arquitectura de e-commerce basada en DDD + Sagas.

---

## 🧰 7. Implementaciones reales del patrón Saga

**Prompt:**

> Muestra ejemplos reales de implementación del patrón Saga usando frameworks como **Temporal.io**, **Camunda**, **Axon Framework**, **NServiceBus** o **Spring Boot Orchestrator**.
> Compara los enfoques de **coreografía vs orquestación** con fragmentos de código reales.
> Analiza cómo cada framework maneja **retries**, **timeouts** y **compensaciones fallidas**.
> Cierra con una recomendación práctica sobre cuál usar según el tamaño y complejidad del sistema.

---

## ⚠️ 8. Tolerancia a fallos y resiliencia

**Prompt:**

> Explica cómo diseñar un sistema de microservicios basado en Sagas con **resiliencia y tolerancia a fallos**.
> Describe patrones complementarios como **Circuit Breaker**, **Retry**, **Outbox**, e **Idempotent Consumers**.
> Usa ejemplos prácticos para mostrar qué pasa si un servicio no responde o si la compensación falla.
> Agrega recomendaciones de monitoreo y observabilidad (por ejemplo, usando OpenTelemetry o Prometheus).

---

## 🧩 9. Alternativas al patrón Saga

**Prompt:**

> Analiza alternativas al patrón Saga para manejar consistencia distribuida:
>
> * **TCC (Try-Confirm-Cancel)**
> * **Workflow orchestration engines**
> * **CQRS (Command Query Responsibility Segregation)**
>   Explica sus ventajas, limitaciones y escenarios de uso frente a Sagas.
>   Termina con un diagrama comparativo que muestre en qué condiciones cada patrón es preferible.

---

## 🧠 10. Coste de complejidad y decisión arquitectónica

**Prompt:**

> Analiza los **trade-offs arquitectónicos** entre usar **Sagas** y mantener un **monolito modular** o una **arquitectura microservicios**.
> Explica cómo el patrón Saga introduce complejidad técnica, pero también escalabilidad organizacional.
> Incluye criterios claros para decidir:
>
> * ¿Cuándo vale la pena usar Sagas?
> * ¿Cuándo es sobreingeniería?
>   Usa ejemplos de startups vs grandes plataformas.

---

## 🧭 Bonus: Prompt para una visión general integradora

**Prompt:**

> Crea un resumen integrador que conecte todos los conceptos relacionados con el patrón Saga:
> transacciones distribuidas, consistencia eventual, DDD, comunicación asíncrona, resiliencia y orquestación.
> Usa ejemplos de arquitectura de microservicios de e-commerce o banca digital.
> Agrega una tabla que muestre cómo cada componente (servicio, evento, compensación, timeout) contribuye a la consistencia global del sistema.

---

¿Quieres que te genere también **un plan de investigación semanal** (por ejemplo, 5 días, 1 hora diaria, con entregables y preguntas de comprensión por tema)?
Eso haría más fácil convertir esta lista de prompts en un programa de estudio práctico.
