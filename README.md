# 🪢 KnotPay: Autonomous Ingestion & Atomic Execution Engine

[🇧🇷 Português (PT-BR)](#-português-pt-br) | [🇺🇸 English (EN-US)](#-english-en-us)

---

## 🇧🇷 Português (PT-BR)

### 🎯 O Conceito: A Aniquilação do Vácuo de Decisão
No ecossistema moderno de e-commerce, arbitragem de ativos digitais e compras industriais (procurement), a informação tem um prazo de validade medido em milissegundos. Tradicionalmente, as empresas operam com "vácuos de decisão": ferramentas monitoram o mercado e geram alertas em dashboards para que um humano, eventualmente, tome a decisão de compra. Até que o clique ocorra, a oportunidade já desapareceu ou o preço foi corrigido.

O **KnotPay** não é um sistema de monitoramento passivo. É um **Motor Autônomo de Arbitragem e Execução Financeira de Consistência Forte**. Ele funde duas disciplinas de engenharia distintas: a hiper-reatividade da extração de dados poliglota (para mapear a web em tempo real) e a hiper-segurança de um motor financeiro transacional (para executar pagamentos sem risco). O sistema lê o mercado, valida a margem de lucro e liquida a transação de forma atômica, sem qualquer intervenção humana.

### 🪢 Por que o nome "KnotPay"?
Em sistemas distribuídos e engenharia mecânica, o maior desafio é amarrar pontas soltas. O **"Knot" (Nó)** representa o ponto físico exato onde duas forças massivas se encontram e são travadas com força máxima, sem folgas.

De um lado, temos o fluxo caótico, bruto e de altíssima velocidade da extração de dados web. Do outro lado, temos a rigidez intransponível e a consistência matemática do livro contábil bancário. O KnotPay é o "nó" que amarra a inteligência de dados à execução de capital. É o ponto onde a informação vira dinheiro líquido, garantindo que o laço nunca se desfaça por falhas de rede ou concorrência.

### ⚙️ Como Tudo Funciona (A Linha de Montagem Tecnológica)
O sistema evita o erro comum do "monolito de scripting". Ele utiliza uma **Arquitetura Poliglota Orientada a Eventos**, onde cada linguagem resolve exclusivamente o problema para o qual foi projetada.

*   **Estágio 1: Ingestão e Radar (Python 3.12):** Utilizamos o ecossistema assíncrono do Python (Scrapy) para gerenciar o ciclo de vida HTTP. Spiders operam 24/7 rotacionando proxies e extraindo dados brutos de concorrentes e fornecedores.
*   **Estágio 2: Refino Térmico e Vetorização (Mojo):** O dado bruto é injetado diretamente em containers rodando **Mojo**. Usando paralelismo e processamento vetorial (SIMD) de baixo nível, o Mojo limpa impurezas de caracteres, converte moedas e tipifica o dataset na memória em nanosegundos.
*   **Estágio 3: O Cérebro de Risco (Ruby 3.3):** O dataset limpo passa por uma DSL em Ruby. O motor de regras de negócio analisa a oportunidade. Se a margem de revenda for positiva, o Ruby gera o "Sinal de Compra".
*   **Estágio 4: O Orquestrador e o Despacho (PHP 8.3 / Laravel 11):** O Laravel atua como o *Control Plane*, auditando a decisão e publicando um evento em uma fila de alta velocidade com uma **Chave de Idempotência** rigorosa.
*   **Estágio 5: O Músculo Financeiro Atômico (Java 21 & PostgreSQL):** O motor financeiro intercepta o evento, ativa uma Máquina de Estados Finita (FSM) e aplica um **Lock Pessimista (`SELECT FOR UPDATE`)** direto no banco de dados. A transação é travada de forma ACID; se a requisição for duplicada, a chave de idempotência a descarta, e se o saldo for insuficiente, as *Check Constraints* do disco abortam a operação.

---

## 🇺🇸 English (EN-US)

### 🎯 The Concept: The Annihilation of the Decision Vacuum
In high-frequency markets—whether it's e-commerce, asset arbitrage, or industrial procurement—the delay between discovering an opportunity and settling the payment is the vacuum where millions are lost. **KnotPay** obliterates this decision latency.

This is not a passive monitoring dashboard or an alert bot. KnotPay is a proprietary autonomous execution infrastructure. The system sweeps the web in milliseconds, sanitizes and validates data profitability through a high-performance polyglot pipeline, and triggers financial liquidation atomically—guaranteeing strong consistency (ACID) and zero risk of double-spending or duplicate orders.

### 🪢 Why the name "KnotPay"?
In distributed systems and mechanical engineering, the greatest challenge is tying up loose ends. The **"Knot"** represents the exact physical point where two massive forces meet and are locked together with maximum strength, leaving no slack.

On one side, we have the chaotic, brute-force, high-velocity stream of web data extraction. On the other side, we have the impenetrable rigidity and mathematical consistency of the banking ledger. KnotPay is the "knot" that ties data intelligence to capital execution. It is the point where information turns into liquid money, ensuring the loop never unravels due to network failures or concurrency race conditions.

### ⚙️ How It Works (The Technological Assembly Line)
The system avoids the "scripting monolith" trap. It uses an **Event-Driven Polyglot Architecture**, where each language exclusively solves the problem it was designed for.

*   **Stage 1: Ingestion and Radar (Python 3.12):** We utilize Python's asynchronous ecosystem (Scrapy) to manage the HTTP lifecycle. Spiders operate 24/7, rotating proxies and extracting raw data from competitors and suppliers.
*   **Stage 2: Thermal Refinement and Vectorization (Mojo):** Raw data is injected directly into containers running **Mojo**. Leveraging advanced vector processing (SIMD), it sanitizes and types datasets in nanoseconds, shielding the CPU from slow bottlenecks.
*   **Stage 3: The Risk Brain (Ruby 3.3):** The clean dataset passes through a Ruby DSL. The business rules engine analyzes the opportunity. If the resale margin is positive, the Ruby engine issues a "Buy Signal".
*   **Stage 4: Orchestration and Dispatch (PHP 8.3 / Laravel 11):** Laravel acts as the *Control Plane*, auditing the purchasing decision and publishing an event to a high-speed message broker with a strict **Idempotency Key**.
*   **Stage 5: The Atomic Financial Muscle (Java 21 & PostgreSQL):** The core financial engine intercepts the event, triggers a Finite State Machine (FSM), and forces a **Pessimistic Lock (`SELECT FOR UPDATE`)** on the database layer. The transaction is locked in an ACID-compliant manner; if the request is duplicated, the idempotency key discards it, and if check constraints fail at disk level, PostgreSQL forces an instant rollback.

---

## 🛠️ Matriz de Especialização / Runtime Specialization Matrix

| Componente / Component | Runtime | Missão Crítica / Critical Mission |
| :--- | :--- | :--- |
| **Ingestion** | Python 3.12 (Scrapy) | Gerenciamento de requisições HTTP, rotação de proxies e extração de DOM. |
| **Refinement** | Mojo | Sanitização de strings e computação vetorial de baixo nível na memória. |
| **Strategy** | Ruby 3.3 | Processamento dinâmico de regras de negócio e cálculo de deltas. |
| **Orchestration** | PHP 8.3 / Laravel 11 | Despacho de Jobs, logs de auditoria e segurança de borda. |
| **Streaming** | RabbitMQ / Kafka | Desacoplamento assíncrono e transporte imutável de eventos. |
| **Settlement** | Java 21 (Spring Boot) | Máquina de Estados Finita (FSM) e orquestração transacional ACID. |
| **Persistence** | PostgreSQL 16 | Locks de linha puros, integridade relacional e barreiras físicas de hardware. |

---

## 📁 Estrutura de Engenharia / Repository Blueprint

```text
KnotPay/
├── .docker/                  # Microservices infrastructure blueprints
│   ├── php-orchestrator/
│   ├── python-scraper/
│   ├── ruby-engine/
│   ├── mojo-core/
│   └── java-financial/
│
├── 1-ingestion-stream/       # The Data Inflow Pipeline
│   ├── scraper-python/       # Asynchronous Web Crawlers
│   ├── core-mojo/            # Low-Level Vector Sanitization
│   ├── engine-ruby/          # Pricing & Opportunity DSL
│   └── control-laravel/      # Audit Logging & Event Dispatcher
│
├── 2-settlement-engine/      # The Financial Vault
│   ├── src/main/java/        # Spring Boot Core Engine
│   │   ├── broker/           # Event Stream Consumers
│   │   ├── state/            # FSM (Finite State Machine) State Enforcement
│   │   └── repository/       # Pessimistic Locking Queries (SELECT FOR UPDATE)
│   └── schema-postgres/      # Table definitions, Row-Locks & Check Constraints
│
├── scripts/                  # Chaos Engineering Labs
│   └── go-stress-test/       # Concurrent Goroutines attempting to force race-conditions
│
├── docker-compose.yml        # Multi-runtime cluster orchestration
└── README.md                 # System Manifesto
