# FluxoScrape: Polyglot Intelligence Ecosystem

![License](https://img.shields.io/github/license/seu-usuario/projetofluxoscrape?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Ruby](https://img.shields.io/badge/Ruby-3.3-CC342D?style=for-the-badge&logo=ruby&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.3-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-11-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-24.0-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-IA-412991?style=for-the-badge&logo=openai&logoColor=white)

---

## 🇧🇷 Português (PT-BR)

### 🎯 Por que este projeto existe? (Missão e Visão)
No mercado digital contemporâneo, a volatilidade de preços é extrema. Empresas que dependem de processos manuais de monitoramento sofrem com a "miopia comercial": quando percebem a movimentação do concorrente, a oportunidade de venda já se dissipou. O **FluxoScrape** foi concebido para ser uma solução de **Inteligência Competitiva Automática**. O objetivo principal é fechar o gap entre a coleta de dados brutos e a tomada de decisão estratégica, utilizando um ecossistema tecnológico que garante que nenhuma informação se perca e que cada insight seja entregue de forma mastigada para o usuário final através de Inteligência Artificial Generativa.

### 💡 Por que ele é interessante? (Diferenciais Estratégicos)
O grande diferencial deste projeto reside na sua **Arquitetura de Microserviços Poliglotas**. Enquanto a maioria dos desenvolvedores tenta forçar uma única linguagem a realizar todas as tarefas — muitas vezes sacrificando performance ou escalabilidade — o FluxoScrape respeita as especialidades de cada stack. Além disso, a implementação de um **Bot de IA Consultivo** no front-end eleva o projeto de um simples script de automação para um produto de prateleira (SaaS), onde a tecnologia complexa é escondida por trás de uma interface conversacional intuitiva e poderosa.

### 🛠 Como o projeto funciona (O Fluxo Profundo do Dado)
O fluxo de dados é estruturado em uma pipeline robusta de quatro estágios:
1.  **Orquestração e Input:** Através do Dashboard construído em Laravel 11, o usuário gerencia o inventário e estabelece parâmetros críticos, como SKUs, URLs de rastreio e thresholds de lucratividade.
2.  **Extração Massiva (Ingestão):** O container Python, operando de forma isolada, executa spiders de alta performance. Ele lida com a limpeza de dados, normalização de strings e conversão de moedas antes de persistir o dado no MySQL.
3.  **Análise e Motor de Regras (Intelligence):** O serviço em Ruby monitora o banco de dados em tempo real. Ele não apenas compara preços, mas calcula tendências e margens líquidas, disparando alertas apenas quando uma ação humana é realmente necessária.
4.  **Interface Conversacional (IA):** O dashboard consome os insights do Ruby e, através de uma ponte API com modelos de linguagem (LLM), o Chatbot traduz tabelas complexas em sugestões verbais como: "Seu concorrente baixou o preço em 10%, mas sua margem permite cobrir a oferta com lucro de 5%. Deseja atualizar?".

### 🧠 Por que cada linguagem para cada ação? (Justificativa Técnica)
*   **Python (A Força Bruta):** Python é a linguagem soberana para Web Scraping. O uso do framework **Scrapy** permite o tratamento de requisições assíncronas, gerenciamento de proxies e contorno de sistemas anti-bot que seriam extremamente complexos de implementar em outras linguagens.
*   **Ruby (A Lógica Elegante):** Ruby foi escolhido para o motor de regras devido à sua filosofia de "felicidade do desenvolvedor" e expressividade. Em sistemas de decisão, onde as regras de negócio mudam constantemente, a facilidade de leitura e manutenção do Ruby (Domain Specific Languages - DSLs) é um ativo inestimável.
*   **PHP / Laravel (O Comando Central):** Para o front-end e gestão de estado, o Laravel oferece o ecossistema mais completo do mercado. Sua segurança robusta, sistema de filas (Queues) e a facilidade de integrar o Vue.js via Vite tornam-no a escolha lógica para um painel administrativo que precisa ser rápido e seguro.

### 📑 Conceitos Aplicados de Engenharia
*   **Conteinerização Multi-Stage:** Uso de Docker para isolar dependências conflitantes (como drivers do Chrome para Python vs drivers de DB para Ruby).
*   **Interoperabilidade de Dados:** Comunicação eficiente entre serviços independentes via camada de persistência compartilhada.
*   **Agentic Thinking:** Design de IA que não apenas responde perguntas, mas analisa o contexto do banco de dados para sugerir ações.
*   **DevOps Culture:** Automação de ambiente completa, permitindo que o projeto seja clonado e rodado com um único comando (`docker-compose up`).

---

## 🇺🇸 English (EN-US)

### 🎯 Why does this project exist? (Mission and Vision)
In today's digital market, price volatility is extreme. Companies relying on manual monitoring suffer from "commercial myopia": by the time they notice a competitor's move, the sales opportunity has already vanished. **FluxoScrape** was designed to be an **Automatic Competitive Intelligence** solution. The primary goal is to close the gap between raw data collection and strategic decision-making, using a technological ecosystem that ensures no information is lost and every insight is delivered in a digestible format to the end user through Generative AI.

### 💡 Why is it interesting? (Strategic Differentials)
The project's key differentiator lies in its **Polyglot Microservices Architecture**. While most developers try to force a single language to perform all tasks — often sacrificing performance or scalability — FluxoScrape respects the specialties of each stack. Furthermore, the implementation of a **Consultative AI Bot** in the front-end elevates the project from a simple automation script to a shelf-ready product (SaaS), where complex technology is hidden behind an intuitive and powerful conversational interface.

### 🛠 How the project works (Deep Data Flow)
The data flow is structured in a robust four-stage pipeline:
1.  **Orchestration and Input:** Through the Dashboard built in Laravel 11, the user manages inventory and sets critical parameters such as SKUs, tracking URLs, and profitability thresholds.
2.  **Massive Extraction (Ingestion):** The Python container, operating in isolation, executes high-performance spiders. It handles data cleaning, string normalization, and currency conversion before persisting the data to MySQL.
3.  **Analysis and Rules Engine (Intelligence):** The Ruby service monitors the database in real-time. It doesn't just compare prices; it calculates trends and net margins, triggering alerts only when human action is truly necessary.
4.  **Conversational Interface (AI):** The dashboard consumes Ruby's insights and, through an API bridge with Large Language Models (LLM), the Chatbot translates complex tables into verbal suggestions like: "Your competitor dropped their price by 10%, but your margin allows you to match it with a 5% profit. Would you like to update?".

### 🧠 Why each language for each action? (Technical Justification)
*   **Python (The Brute Force):** Python is the sovereign language for Web Scraping. Using the **Scrapy** framework allows for handling asynchronous requests, proxy management, and bypassing anti-bot systems that would be extremely complex to implement in other languages.
*   **Ruby (The Elegant Logic):** Ruby was chosen for the rules engine due to its "developer happiness" philosophy and expressiveness. In decision systems where business rules change constantly, Ruby's readability and ease of maintenance (Domain Specific Languages - DSLs) are invaluable assets.
*   **PHP / Laravel (The Central Command):** For the front-end and state management, Laravel offers the most complete ecosystem on the market. Its robust security, task queuing system, and ease of integrating Vue.js via Vite make it the logical choice for an admin panel that needs to be fast and secure.

### 📑 Applied Engineering Concepts
*   **Multi-Stage Containerization:** Use of Docker to isolate conflicting dependencies (such as Chrome drivers for Python vs DB drivers for Ruby).
*   **Data Interoperability:** Efficient communication between independent services via a shared persistence layer.
*   **Agentic Thinking:** AI design that doesn't just answer questions but analyzes database context to suggest actions.
*   **DevOps Culture:** Complete environment automation, allowing the project to be cloned and run with a single command (`docker-compose up`).

---

## 📁 Estrutura de Pastas / Project Structure
```text
PROJETOFLUXOSCRAPE/
│
├── .docker/                # Infrastructure blueprints (Dockerfiles)
│   ├── php/                # PHP 8.3 & Apache environment
│   ├── python/             # Python 3.12 & Scraping tools
│   └── ruby/               # Ruby 3.3 & Logic Engine environment
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
│   ├── spiders/            # Scrapy bots for different targets
│   ├── services/           # DB Connectors & Cleaners
│   └── main.py             # Execution Orchestrator
│
├── .env                    # Environment variables (API Keys, DB Credentials)
├── docker-compose.yml      # The "Master Key" orchestrating the stack
└── README.md               # Documentation and technical overview
