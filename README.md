# 🚀 FluxoScrape: Polyglot Intelligence Ecosystem

![License](https://img.shields.io/github/license/seu-usuario/projetofluxoscrape?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Mojo](https://img.shields.io/badge/Mojo-white?style=for-the-badge&logo=mojo&logoColor=FF4B12)
![Ruby](https://img.shields.io/badge/Ruby-3.3-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.3-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-11-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-24.0-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-IA-412991?style=for-the-badge&logo=openai&logoColor=white)

---

## 🇧🇷 Português (PT-BR)

### 🎯 Por que este projeto existe? (A Crise da Reatividade e a Solução Preditiva)
No ecossistema de e-commerce moderno, a informação tem um prazo de validade extremamente curto. O projeto **FluxoScrape** não nasceu apenas como uma ferramenta de automação, mas como uma resposta à **Crise da Reatividade Comercial**. 

Tradicionalmente, empresas monitoram concorrentes de forma passiva ou através de ferramentas que entregam relatórios estáticos. Quando um gestor recebe um alerta de que seu preço está 15% acima do mercado, ele já perdeu milhares de conversões nas últimas horas. Existe um "vácuo de decisão" entre o fato (a mudança de preço do concorrente) e a ação (o ajuste no seu dashboard). Este projeto existe para **aniquilar essa latência**. Ele transforma o processo de monitoramento em um ciclo de Inteligência de Fluxo Contínuo, permitindo que a tecnologia tome o trabalho pesado de mineração e cálculo, deixando para o humano apenas a decisão final estratégica.

### 💡 O Diferencial da Engenharia Poliglota (Arquitetura de Alta Disponibilidade)
O verdadeiro diferencial deste projeto não é o que ele faz, mas **como** ele foi construído. Fugimos da armadilha do "Monolito de Scripting" para adotar uma **Engenharia Heterogênea**. A maioria das soluções de mercado falha na escalabilidade porque tentam processar dados massivos em linguagens de alto nível que sofrem com gargalos de memória ou CPU.

*   **Especialização de Runtime:** Utilizamos o **Python** exclusivamente para o que ele é imbatível: o ecossistema de bibliotecas de rede e navegação web (Scrapy).
*   **Computação de Baixo Nível:** Introduzimos o **Mojo** para atuar onde o Python falha. O Mojo permite o acesso ao poder do hardware (vetorização e paralelismo) sem a complexidade do C++, garantindo limpeza de dados em tempo real.
*   **Abstração de Negócio:** Reservamos o **Ruby** para a lógica financeira. A expressividade do Ruby permite criar uma DSL (*Domain Specific Language*) para regras de preço, tornando o sistema adaptável em minutos.
*   **Sólida Interface de Gestão:** O **Laravel** fecha o ciclo provendo uma base de segurança corporativa, gestão de filas e persistência de dados madura.

### 🛠 Anatomia do Fluxo de Dados (A Pipeline de Inteligência)
O fluxo segue o princípio de **ETL Reativo (Extract, Transform, Load)**, operando em microserviços orquestrados por Docker:

1.  **Camada de Ingestão (Python/Scrapy):** Spiders assíncronas extraem dados não estruturados lidando com rotação de proxies e parsing de DOM complexos para gerar JSONs estruturados.
2.  **Camada de Refino Térmico (Mojo):** O dado bruto é injetado no motor Mojo para operações de *Type-Safety* e *Data Normalization* em nível de memória, preparando datasets sem travar o sistema.
3.  **Camada de Persistência e Estado (MySQL/Laravel):** Dados refinados são persistidos em esquema relacional otimizado, onde o Laravel monitora mudanças e gerencia o histórico temporal (*Time Series*).
4.  **Camada de Inteligência de Negócio (Ruby Engine):** O Ruby executa o motor de regras financeiras, comparando preços de mercado com custos e estoque para gerar Oportunidades Comerciais.
5.  **Camada de Entrega e Agente de IA (OpenAI/Vue.js):** O dado vira linguagem natural. A API da OpenAI processa o contexto e apresenta uma análise cognitiva: "Detectamos uma queda no concorrente A. Deseja aplicar o ajuste?".

---

## 🇺🇸 English (EN-US)

### 🎯 Why does this project exist? (The Crisis of Reactivity)
In the modern e-commerce landscape, information has an extremely short shelf life. **FluxoScrape** was born as a response to the **Commercial Reactivity Crisis**. 

Traditionally, companies monitor competitors passively. By the time a manager notices a price gap, thousands of conversions are already lost. There is a "decision vacuum" between the fact and the action. This project exists to **annihilate this latency**. It transforms monitoring into a Continuous Flow Intelligence cycle, allowing technology to handle the heavy lifting of mining and calculation, leaving only the final strategic decision to the human element.

### 💡 Strategic Polyglot Architecture (High Availability)
The true differentiator of this project is not what it does, but **how** it was built. We avoid the "Scripting Monolith" trap by adopting **Heterogeneous Engineering**. Most market solutions fail to scale because they attempt to process massive data in high-level languages that suffer from memory or CPU bottlenecks.

*   **Runtime Specialization:** We use **Python** for what it does best: the ecosystem of network libraries and web navigation (Scrapy).
*   **Low-Level Computing:** We introduced **Mojo** to step in where Python fails. Mojo allows access to hardware power (vectorization and parallelism) without C++ complexity, ensuring real-time data cleaning.
*   **Business Abstraction:** **Ruby** is reserved for financial logic. Ruby's expressiveness allows for the creation of a DSL (*Domain Specific Language*) for pricing rules, making the system adaptable in minutes.
*   **Management Interface:** **Laravel** provides the corporate security base, queue management, and mature data persistence.

### 🛠 Detailed Data Flow (The Intelligence Pipeline)
The data flow follows the **Reactive ETL (Extract, Transform, Load)** principle, operating in microservices orchestrated by Docker:

1.  **Ingestion Layer (Python/Scrapy):** Asynchronous spiders extract unstructured data, handling proxy rotation and complex DOM parsing to generate structured JSON.
2.  **Thermal Refinement Layer (Mojo):** Raw data is injected into the Mojo engine for memory-level **Type-Safety** and **Data Normalization**, preparing datasets without locking the system.
3.  **Persistence & State Layer (MySQL/Laravel):** Refined data is persisted in an optimized relational schema, where Laravel monitors changes and manages time-series history.
4.  **Business Intelligence Layer (Ruby Engine):** Ruby executes the financial rules engine, comparing market prices with costs and inventory to generate Commercial Opportunities.
5.  **AI Consultative Layer (OpenAI/Vue.js):** Data turns into natural language. The OpenAI API processes the context and presents a cognitive analysis: "We detected a drop in competitor A. Would you like to apply the adjustment?".

---

### (PT-BR)  Por que cada linguagem para cada ação? (Arquitetura Profunda)

#### 🐍 Python 3.12 (A Camada de Interação com o DOM)
O Python não foi escolhido por sua velocidade, mas por seu ecossistema de rede. A camada de raspagem exige resiliência contra bloqueios.
*   **Como age:** O container Python utiliza o framework Scrapy e bibliotecas de processamento de sinais para simular o comportamento humano. Ele gerencia o ciclo de vida das requisições HTTP, rotaciona cabeçalhos (User-Agents) e resolve desafios de renderização via middleware.
*   **Responsabilidade:** Navegar pela estrutura de árvore do HTML (DOM), extrair seletores CSS/XPath e converter o caos visual da web em dicionários de dados brutos e estruturados.

#### 🔥 Mojo (O Motor de Computação e Vetorização)
Aqui o projeto atinge performance de nível de sistema. O Mojo entra para resolver o gargalo de processamento que o Python criaria ao lidar com milhões de pontos de dados.
*   **Como age:** O Mojo utiliza SIMD (Single Instruction, Multiple Data) para processar vetores de dados simultaneamente. Ele age diretamente na memória do container, realizando a normalização de strings, sanitização de caracteres especiais e cálculos de conversão de câmbio em nanosegundos.
*   **Responsabilidade:** Atuar como um filtro de alta vazão. Ele recebe o "entulho" de dados do Python e entrega um dataset limpo e tipado para o banco de dados, garantindo que a CPU não seja sobrecarregada por loops lentos.

#### 💎 Ruby 3.3 (A Máquina de Estado e Regras de Negócio)
O Ruby é a linguagem da expressividade. Em sistemas de precificação, as regras de negócio mudam conforme a estratégia de marketing.
*   **Como age:** O Ruby consome os dados persistidos e os passa por um motor de lógica (Rules Engine). Graças à sua natureza altamente dinâmica, ele permite definir algoritmos complexos — como o "Price Elasticity" — de forma quase verbal. Ele age comparando o delta de preços entre o passado e o presente.
*   **Responsabilidade:** Inteligência lógica. Ele decide se uma alteração de preço é uma anomalia (erro do concorrente) ou uma tendência real de mercado, gerando o sinal que alimentará a IA.

#### 🐘 PHP 8.3 / Laravel 11 (O Orquestrador de Infraestrutura)
O Laravel não é apenas o "site", é o Control Plane do ecossistema.
*   **Como age:** O Laravel gerencia os Jobs e Queues (filas de trabalho). Ele coordena quando os scrapers devem rodar, garante a segurança da API que se comunica com a OpenAI e mantém a integridade das sessões dos usuários. Através do Eloquent ORM, ele abstrai a complexidade do banco de dados MySQL para os outros containers.
*   **Responsabilidade:** Interface administrativa, segurança, gestão de tarefas agendadas e integração com o frontend Vue.js para o Chatbot de IA.

---
###  (EN-US) Why each language for each action? (Deep Architecture)

#### 🐍 Python 3.12 (DOM Interaction Layer)
Python was not chosen for speed, but for its networking ecosystem. The scraping layer requires resilience against bot detection.
*   **How it acts:** The Python container uses the Scrapy framework to simulate human behavior. It manages the HTTP request lifecycle, rotates headers (User-Agents), and solves rendering challenges via specialized middleware.
*   **Responsibility:** Navigating the HTML tree structure (DOM), extracting CSS/XPath selectors, and converting web chaos into structured raw data dictionaries.

#### 🔥 Mojo (Computation and Vectorization Engine)
This is where the project reaches system-level performance. Mojo is introduced to solve the processing bottleneck that Python would create when dealing with millions of data points.
*   **How it acts:** Mojo utilizes SIMD (Single Instruction, Multiple Data) to process data vectors simultaneously. It acts directly on the container’s memory, performing string normalization, sanitization, and currency conversion calculations in nanoseconds.
*   **Responsibility:** Acting as a high-throughput filter. It receives the data "debris" from Python and delivers a clean, typed dataset to the database, ensuring the CPU is not bogged down by slow loops.

#### 💎 Ruby 3.3 (State Machine and Business Rules)
Ruby is the language of expressiveness. In pricing systems, business rules shift according to marketing strategies.
*   **How it acts:** Ruby consumes the persisted data and passes it through a Rules Engine. Thanks to its highly dynamic nature, it allows for defining complex algorithms — such as Price Elasticity — in a near-verbal way. It calculates the price delta between past and present values.
*   **Responsibility:** Logical intelligence. It decides if a price change is an anomaly (competitor error) or a real market trend, generating the signal that feeds the AI.

#### 🐘 PHP 8.3 / Laravel 11 (Infrastructure Orchestrator)
Laravel is not just the "website"; it is the Control Plane of the ecosystem.
*   **How it acts:** Laravel manages Jobs and Queues. It coordinates when scrapers should run, secures the API communication with OpenAI, and maintains user session integrity. Through Eloquent ORM, it abstracts the MySQL database complexity for the other containers.
*   **Responsibility:** Admin interface, security, scheduled task management, and Vue.js frontend integration for the AI Chatbot.

---















## 📁 Estrutura de Pastas / Project Structure
```text
PROJETOFLUXOSCRAPE/
│
├── .docker/                # Infrastructure blueprints (Dockerfiles)
│   ├── php/                # PHP 8.3 & Apache environment
│   ├── python/             # Python 3.12 & Scraping tools
│   ├── ruby/               # Ruby 3.3 & Logic Engine environment
│   └── mojo/               # Mojo SDK & Performance environment
│
├── core-mojo/              # High-Performance Engine (Mojo)
│   ├── src/                # Heavy data processing logic
│   └── main.mojo           # Entry point for fast computation
│
├── dashboard-php/          # Control Center (Laravel 11)
│   ├── app/                # Business Logic & AI Bridges
│   ├── resources/js/       # Frontend (Vue.js ChatBot)
│   └── database/           # Schema and Migrations
│
├── engine-ruby/            # Decision Engine (Ruby 3.3)
│   ├── lib/                # Analytical classes
│   └── processor.rb        # Background worker for data analysis
│
├── scraper-python/         # Data Harvesters (Python 3.12)
│   ├── spiders/            # Scrapy bots
│   └── main.py             # Orchestrator
│
├── .env                    # API Keys & DB Credentials
├── docker-compose.yml      # The "Master Key" orchestrating the stack
└── README.md               # Documentation
