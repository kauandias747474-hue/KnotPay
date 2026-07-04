Aqui estão os comandos para criar a nova estrutura de diretórios (sem Mojo) no seu Windows e o README inteiro refeito em português e inglês.

---

## 📂 Comandos para criar a estrutura (VS Code / PowerShell)

Abra o terminal do VS Code (PowerShell) na raiz do projeto (`KnotPay/`) e execute os comandos abaixo. Eles criarão as pastas necessárias, mantendo a organização original, mas removendo `mojo/` e `core-mojo/`, e adicionando um módulo de sanitização dentro do scraper.

```powershell
# Raiz do projeto (certifique-se de estar em KnotPay/)
mkdir .docker, dashboard, 1-ingestion-stream, 2-settlement-engine, scripts

# Subpastas principais
mkdir .docker\php-orchestrator, .docker\python-scraper, .docker\ruby-engine, .docker\java-financial
mkdir dashboard\resources\css, dashboard\resources\js\components, dashboard\routes
mkdir 1-ingestion-stream\scraper-python\services, 1-ingestion-stream\scraper-python\spiders, 1-ingestion-stream\scraper-python\utils
mkdir 1-ingestion-stream\engine-ruby\lib\rules
mkdir 1-ingestion-stream\control-laravel   # substitui o antigo "control-laravel"
mkdir 2-settlement-engine\src\main\java\broker, 2-settlement-engine\src\main\java\state, 2-settlement-engine\src\main\java\repository
mkdir 2-settlement-engine\schema-postgres
mkdir scripts\go-stress-test

# Remova referências ao Mojo (caso existam)
# Remove-Item -Recurse -Force .\mojo, .\core-mojo -ErrorAction SilentlyContinue
```

**Observação:** Execute o comando `Remove-Item` apenas se ainda houver resquícios das pastas antigas. Agora a limpeza dos dados fica em `scraper-python/utils/sanitizer.py`.

---

## 📖 README completo (PT-BR + EN-US)

Substitua o conteúdo atual do `README.md` pelo texto abaixo. Ele mantém o manifesto arquitetural, mas remove a dependência do Mojo e reposiciona a etapa de refino para Python.

```markdown
# 🪢 KnotPay: Autonomous Ingestion & Atomic Execution Engine

🇧🇷 Português (PT-BR) | 🇺🇸 English (EN-US)

---

## 🇧🇷 Português (PT-BR)

### ⚠️ Aviso de Estudo Arquitetural
Este repositório é um projeto de pesquisa arquitetural, explorando os limites de pipelines transacionais de alta frequência. O objetivo é avaliar a interoperabilidade entre diferentes runtimes e os trade-offs de performance de uma abordagem poliglota. **Trata‑se de um protótipo conceitual e um projeto de arquitetura em desenvolvimento.**

---

### 🎯 O Conceito: A Aniquilação do Vácuo de Decisão
No ecossistema moderno de e‑commerce, arbitragem de ativos digitais e compras industriais, a informação tem um prazo de validade medido em milissegundos. Sistemas tradicionais geram alertas em dashboards para que um humano tome a decisão – o “vácuo” onde as oportunidades evaporam.

**O KnotPay não é um sistema de monitoramento passivo.** É um Motor Autônomo de Arbitragem e Execução Financeira de Consistência Forte. Ele funde duas disciplinas: hiper‑reatividade da extração poliglota (mapeamento da web em tempo real) e hiper‑segurança de um motor financeiro transacional (execução de pagamentos sem risco). O sistema lê o mercado, valida a margem e liquida a transação atomicamente, **sem intervenção humana**.

---

### 🪢 Por que o nome "KnotPay"?
Em sistemas distribuídos e engenharia mecânica, o maior desafio é amarrar pontas soltas. O “Knot” (Nó) representa o ponto exato onde duas forças massivas se encontram e são travadas com força máxima – sem folgas.

De um lado, o fluxo caótico e de altíssima velocidade da extração de dados web. Do outro, a rigidez matemática do livro contábil bancário. O KnotPay é o **nó** que amarra a inteligência de dados à execução de capital. É o ponto onde a informação vira dinheiro líquido, garantindo que o laço nunca se desfaça por falhas de rede ou concorrência.

---

### ⚙️ Como Tudo Funciona (A Linha de Montagem Tecnológica)
Utilizamos uma **Arquitetura Poliglota Orientada a Eventos**, onde cada linguagem resolve exclusivamente o problema para o qual foi projetada.

| Estágio | Componente | Runtime | Missão |
|--------|------------|---------|--------|
| 1 | Ingestão & Radar | Python 3.12 (Scrapy) | Gerenciamento de requisições HTTP, rotação de proxies e extração de DOM. |
| 2 | Refino & Sanitização | Python 3.12 (Pandas/Pydantic) | Limpeza de dados, tipagem e normalização de moedas – operações vetorizadas em memória. |
| 3 | Cérebro de Risco | Ruby 3.3 | DSL de regras de negócio, cálculo de margens e geração do “Sinal de Compra”. |
| 4 | Orquestração | PHP 8.3 / Laravel 11 | Control plane, auditoria e disparo de eventos com Chave de Idempotência. |
| 5 | Músculo Financeiro | Java 21 + PostgreSQL | Máquina de Estados Finita (FSM), locks pessimistas (`SELECT FOR UPDATE`) e barreiras ACID. |

**Fluxo resumido:**  
`Scrapy (extração) → Python (sanitização) → Ruby (decisão) → Laravel (orquestração) → Java + PostgreSQL (liquidação)`

---

### 🛠️ Matriz de Especialização Atualizada
| Componente | Runtime | Missão Crítica |
|------------|---------|----------------|
| **Ingestion** | Python 3.12 (Scrapy) | Requisições assíncronas, rotação de proxies, extração de dados brutos. |
| **Refinement** | Python 3.12 (Pandas, NumPy) | Limpeza, conversão de moedas, validação e tipagem dos dados. |
| **Strategy** | Ruby 3.3 | Processamento dinâmico de regras e cálculo de delta de lucro. |
| **Orchestration** | PHP 8.3 / Laravel 11 | Despacho de jobs, logs imutáveis e segurança de borda. |
| **Streaming** | RabbitMQ / Kafka | Desacoplamento assíncrono e transporte imutável de eventos. |
| **Settlement** | Java 21 (Spring Boot) | Máquina de estados finita e orquestração transacional ACID. |
| **Persistence** | PostgreSQL 16 | Locks de linha, integridade relacional e constraints físicas. |

---

### 🐍 Ouroboros: Autonomous Immune System & Resilience Fuzzer
*(Sistema Imunológico Autônomo e Fuzzer de Resiliência)*

####  O Conceito: Autoevolução Adversarial
O módulo **Ouroboros** transforma a infraestrutura do KnotPay de um motor estático em um organismo que aprende e se defende sozinho. Em vez de depender de assinaturas de ataques conhecidos, ele trata todo o pipeline como um laboratório controlado: simula ataques contra a própria lógica de negócio para descobrir vulnerabilidades (0‑days) antes de agentes externos.

####  A Filosofia do Nome: O Ciclo Infinito
- **Crescimento pelo consumo próprio:** O sistema realimenta tráfego real no fuzzer para estressar suas entranhas.  
- **Ciclo eterno:** Segurança não é um estado, é um processo – o Ouroboros devora seus próprios outputs e renasce mais forte a cada teste.  
- **Fechamento do nó:** Tensiona cada ponto de transição dados‑capital, eliminando folgas.

####  Como Funciona Dentro do KnotPay
1. **Espelhamento de contexto** – aprende a gramática esperada dos protocolos.  
2. **Mutação em memória (Python + C extensions)** – bit‑flipping, integer overflows, testes de limites.  
3. **Agente de Reinforcement Learning** – observa a FSM; se um estado ilegal é atingido, registra a sequência exata.  
4. **Vacinação automatizada** – gera um filtro compilado que é injetado na Camada de Ingestão, descartando ataques similares na borda.

---

###  Engenharia do Caos e Rigor Operacional
O KnotPay não é mantido por testes unitários passivos, mas por uma cultura de **Engenharia do Caos** agressiva. O Ouroboros executa ataques simulados continuamente, forçando o sistema a provar sua estabilidade sob falhas de rede, latência ou injeção de pacotes maliciosos. Medimos o sucesso pela capacidade de manter a atomicidade (ACID) mesmo quando tudo ao redor falha.

---

## 🇺🇸 English (EN-US)

### ⚠️ Conceptual Architecture Study
This repository is an architectural research project exploring the boundaries of high‑frequency transactional pipelines. It evaluates interoperability between different runtimes and the performance tradeoffs of a polyglot approach. **This is a conceptual prototype and an ongoing architectural blueprint.**

---

### 🎯 The Concept: The Annihilation of the Decision Vacuum
In high‑frequency markets, the delay between discovery and settlement is where millions are lost. KnotPay obliterates this decision latency.

**KnotPay is not a passive monitoring dashboard.** It is an Autonomous Arbitrage & Financial Execution Engine with strong consistency. It fuses two disciplines: hyper‑reactive polyglot data extraction (real‑time web mapping) and hyper‑secure transactional finance (risk‑free payment execution). The system reads the market, validates profitability, and settles atomically – **with zero human intervention**.

---

### 🪢 Why the name "KnotPay"?
In distributed systems and mechanical engineering, the greatest challenge is tying up loose ends. The “Knot” is the exact point where two massive forces are locked together with maximum strength, leaving no slack.

On one side: the chaotic, high‑velocity stream of web data extraction. On the other: the impenetrable rigidity of the banking ledger. KnotPay is the knot that ties data intelligence to capital execution – the point where information becomes liquid money, ensuring the loop never unravels.

---

### ⚙️ How It Works (The Technological Assembly Line)
We use an **Event‑Driven Polyglot Architecture**, each language solving exactly the problem it was designed for.

| Stage | Component | Runtime | Mission |
|-------|-----------|---------|---------|
| 1 | Ingestion & Radar | Python 3.12 (Scrapy) | HTTP lifecycle management, proxy rotation, DOM extraction. |
| 2 | Refinement & Sanitization | Python 3.12 (Pandas/Pydantic) | Data cleaning, currency conversion, typing – in‑memory vectorized operations. |
| 3 | Risk Brain | Ruby 3.3 | Business rule DSL, margin calculation, “Buy Signal” generation. |
| 4 | Orchestration | PHP 8.3 / Laravel 11 | Control plane, audit logging, idempotent event dispatch. |
| 5 | Financial Muscle | Java 21 + PostgreSQL | Finite State Machine (FSM), pessimistic locking (`SELECT FOR UPDATE`), ACID barriers. |

**Summary flow:**  
`Scrapy (extraction) → Python (sanitization) → Ruby (decision) → Laravel (orchestration) → Java + PostgreSQL (settlement)`

---

###  Runtime Specialization Matrix (Updated)
| Component | Runtime | Critical Mission |
|-----------|--------|------------------|
| **Ingestion** | Python 3.12 (Scrapy) | Asynchronous HTTP, proxy rotation, raw data extraction. |
| **Refinement** | Python 3.12 (Pandas, NumPy) | Cleaning, currency conversion, validation, and typing. |
| **Strategy** | Ruby 3.3 | Dynamic rule processing and profit delta calculation. |
| **Orchestration** | PHP 8.3 / Laravel 11 | Job dispatch, immutable logs, edge security. |
| **Streaming** | RabbitMQ / Kafka | Asynchronous decoupling, immutable event transport. |
| **Settlement** | Java 21 (Spring Boot) | Finite state machine and ACID transactional orchestration. |
| **Persistence** | PostgreSQL 16 | Row locks, relational integrity, hardware‑level constraints. |

---

### 🐍 Ouroboros: Autonomous Immune System & Resilience Fuzzer

####  The Concept: Adversarial Self‑Evolution
The **Ouroboros** module transforms KnotPay from a static engine into a self‑learning organism. Instead of relying on known attack signatures, it treats the entire pipeline as a controlled lab, continuously simulating adversarial attacks to discover zero‑day vulnerabilities before any outsider.

####  Philosophy of the Name: The Infinite Loop
- **Growth through self‑consumption:** Real production traffic is fed back into the fuzzer to stress‑test internal logic.  
- **Eternal cycle:** Security is a process, not a state – Ouroboros devours its own outputs and reborns stronger after every test.  
- **Closing the knot:** It tensions every data‑to‑capital transition point, eliminating any slack.

####  How It Works Inside KnotPay
1. **Context mirroring** – learns the expected grammar of incoming protocols.  
2. **In‑memory mutation (Python + C extensions)** – bit‑flipping, integer overflows, boundary tests.  
3. **Reinforcement Learning agent** – watches the FSM; if an illegal state is reached, it records the exact input sequence.  
4. **Automated vaccination** – generates a compiled filter injected at the Ingestion Layer, blocking similar attack variants at the edge.

---

###  Chaos Engineering & Operational Rigor
KnotPay is maintained not by passive unit tests but by an aggressive **Chaos Engineering** culture. Ouroboros continuously runs simulated attacks, forcing the system to prove its stability under network failures, latency spikes, or malicious packet injection. Success is measured by the ability to preserve transactional atomicity (ACID) even when everything around it breaks.

---

## 📁 Repository Blueprint (Updated)
```
KnotPay/
├── .docker/                  # Microservices infrastructure blueprints
│   ├── php-orchestrator/
│   ├── python-scraper/
│   ├── ruby-engine/
│   └── java-financial/
│
├── 1-ingestion-stream/       # The Data Inflow Pipeline
│   ├── scraper-python/       # Async crawlers + data sanitization
│   ├── engine-ruby/          # Pricing & Opportunity DSL
│   └── control-laravel/      # Audit logging & Event Dispatcher
│
├── 2-settlement-engine/      # The Financial Vault
│   ├── src/main/java/        # Spring Boot Core Engine
│   │   ├── broker/           # Event Stream Consumers
│   │   ├── state/            # FSM State Enforcement
│   │   └── repository/       # Pessimistic Locking Queries
│   └── schema-postgres/      # Table definitions, Row‑Locks & Check Constraints
│
├── dashboard/                # Vue.js front‑end
│   └── resources/...
│
├── scripts/                  # Chaos Engineering Labs
│   └── go-stress-test/       # Concurrent Goroutines race‑condition testing
│
├── docker-compose.yml        # Multi‑runtime cluster orchestration
└── README.md                 # This manifesto
```

---

## 🚀 Join the Evolution / Junte‑se à Evolução

**PT‑BR:** Buscamos colaboradores que entendam a sinergia entre desempenho bruto (Python), resiliência de estado (Java) e inteligência de orquestração (AI/ML). Se você domina a arte de construir sistemas “indestrutíveis”, o KnotPay é o seu laboratório.

**EN:** We seek collaborators who understand the synergy between raw performance (Python), state resilience (Java), and orchestration intelligence (AI/ML). If you master the art of building “indestructible” systems, KnotPay is your laboratory.
```

---
