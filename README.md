# Investigación enfocada para tener una visión completa y práctica sobre **el patrón Saga y su contexto en sistemas distribuidos**.

Aquí tienes una lista priorizada de **temas que deberías investigar**, junto con **por qué** son relevantes según las ideas del hilo:

---

### 🧩 1. Fundamentos del patrón **Saga**

**Qué investigar:**

* Definición del patrón Saga (coreografía vs. orquestación).
* Cómo maneja las **transacciones distribuidas** sin bloqueo.
* Ejemplos de flujos tipo “pedido → pago → envío”.
* Concepto de **acciones compensatorias** (rollback lógico).

**Por qué:**
Es el tema central del hilo. Los comentarios destacan la diferencia entre la idea ideal (tutorial) y la realidad (sistemas complejos, errores, fallos parciales).

---

### ⚙️ 2. **Transacciones distribuidas vs. Sagas**

**Qué investigar:**

* Diferencias entre **2PC (Two-Phase Commit)** y **Saga pattern**.
* Cuándo usar uno u otro.
* Problemas de latencia, bloqueo y disponibilidad en 2PC.

**Por qué:**
Varios comentarios (p. ej. *jacobb11* y *ValuableCockroach993*) lo discuten directamente. Entender por qué Sagas existen como alternativa a 2PC es esencial.

---

### 🔀 3. **Modelos de comunicación asíncrona y eventos**

**Qué investigar:**

* Event-driven architecture (EDA).
* *Message brokers* (Kafka, RabbitMQ, Pub/Sub, etc.).
* Garantías de entrega (“at least once”, “exactly once”).
* Idempotencia en microservicios.

**Por qué:**
Sagas dependen de **mensajería asíncrona y eventos**. Los comentarios mencionan cómo los eventos retrasados o fallos de servicios afectan la consistencia.

---

### 🧱 4. **Event sourcing vs. Saga pattern**

**Qué investigar:**

* Qué es *Event Sourcing* y qué problema resuelve.
* Diferencias entre event sourcing, event-driven y Sagas.
* Cómo pueden coexistir o complementarse.

**Por qué:**
Un usuario confunde ambos patrones (lo que es muy común). Entender esta diferencia te da una ventaja conceptual para explicarlo o aplicarlo correctamente.

---

### 🧠 5. **Consistencia eventual y compensación**

**Qué investigar:**

* Modelos de consistencia en sistemas distribuidos.
* Cómo aplicar *compensating transactions*.
* Estrategias de “retry”, *dead letter queues* y *timeouts*.

**Por qué:**
Sagas no garantizan consistencia inmediata, sino eventual. Es clave saber cómo se maneja la corrección a lo largo del tiempo.

---

### 🧩 6. **Diseño de límites (Bounded Contexts / DDD)**

**Qué investigar:**

* *Domain-Driven Design (DDD)*: conceptos de *bounded context* y *context mapping*.
* Cómo DDD guía la división entre servicios y bases de datos.

**Por qué:**
El comentario de *induality* toca el tema crucial: la **complejidad real está en los datos** y sus límites. Esto conecta directamente con por qué surgen las Sagas.

---

### 🧰 7. **Implementaciones reales del patrón Saga**

**Qué investigar:**

* Frameworks o librerías que soportan Sagas (por ejemplo:

  * **Temporal.io**
  * **Camunda**
  * **Axon Framework**
  * **NServiceBus**
  * **Spring Boot + Orchestrator pattern**)
* Patrones de orquestación vs. coreografía en código.

**Por qué:**
El hilo menciona que los tutoriales simplifican demasiado. Ver implementaciones reales te muestra cómo manejar casos límite (retries, fallbacks, compensaciones fallidas).

---

### ⚠️ 8. **Tolerancia a fallos y resiliencia**

**Qué investigar:**

* Estrategias para manejar fallos parciales:

  * *Circuit Breaker pattern*
  * *Retry pattern*
  * *Outbox pattern*
  * *Idempotent consumers*
* Diseño para resiliencia en microservicios.

**Por qué:**
Muchos comentarios mencionan los retos de “qué pasa si un servicio no responde”, “qué pasa si el rollback falla”, o “cómo mantener consistencia tras fallos”.

---

### 🧩 9. **Alternativas al patrón Saga**

**Qué investigar:**

* *TCC (Try-Confirm/Cancel)* pattern.
* *Workflow orchestration engines*.
* *CQRS* (Command Query Responsibility Segregation).

**Por qué:**
Entender otras formas de manejar consistencia distribuida te da contexto sobre cuándo **Sagas es o no la mejor opción**.

---

### 🧠 10. **Coste de complejidad y decisión arquitectónica**

**Qué investigar:**

* Monolito modular vs. microservicios.
* Cuándo conviene dividir un sistema.
* Trade-offs de complejidad, despliegue, y organización de equipos.

**Por qué:**
El primer comentario del hilo lo resume bien: **no siempre necesitas microservicios**, y usar Sagas puede ser una sobreingeniería si tu sistema es pequeño.

---

### 📚 Plan de estudio en 1 hora

| Tiempo    | Tema                                                       | Objetivo rápido                     |
| --------- | ---------------------------------------------------------- | ----------------------------------- |
| 0–10 min  | Leer sobre el patrón Saga (coreografía vs orquestación).   | Entender el concepto base.          |
| 10–25 min | Comparar Saga vs 2PC y leer sobre consistencia eventual.   | Entender por qué existe.            |
| 25–40 min | Revisar ejemplos de implementación (Temporal.io o Spring). | Ver la complejidad práctica.        |
| 40–55 min | Estudiar diferencias con Event Sourcing y DDD.             | Conectar con el diseño de dominios. |
| 55–60 min | Reflexión: ¿cuándo usarías (o no) Sagas en tu sistema?     | Aplicar criterio arquitectónico.    |

---

¿Quieres que te prepare una **guía de lectura condensada (con links técnicos actuales y diagramas)** para cubrir exactamente esos temas en 1 hora? Podría incluir recursos de Temporal, Camunda y artículos de Martin Fowler.
