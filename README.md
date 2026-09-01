<div align="center">

# 👋 Hi, I'm Élzio

### Senior Backend Engineer · Java · Distributed Systems · AI-Assisted Software Engineering

I build backend systems, developer tools, AI-assisted workflows, and experiments focused on making software engineering more efficient, observable, scalable, and easier for both humans and coding agents to understand.

<br>

![Java](https://img.shields.io/badge/Java-21%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![AI](https://img.shields.io/badge/AI-Agentic%20Development-7C3AED?style=for-the-badge)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Cloud%20Native-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-Streaming-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)

</div>

---

## 🚀 Featured Projects

<table>
<tr>
  <td width="50%" valign="top">
  
  ### 🧠 [AI Context Generation](https://github.com/ElzioJunior/ai-context-generation)
  
  A **vendor-agnostic workflow for building and maintaining an AI-readable knowledge base directly inside software repositories**.
  
  Instead of forcing coding agents to rediscover the architecture, business rules, testing strategy, conventions, and project decisions on every interaction, the project creates persistent, structured context that can evolve together with the codebase.
  
  **Highlights**
  
  - 🤖 Designed specifically for AI coding agents
  - 📚 Generates structured project knowledge covering architecture, business context, domain model, patterns, coding standards, testing strategy, features, decisions, glossary, and open questions
  - 🔄 Supports both initial context generation and incremental updates
  - 🔒 Repository-grounded and evidence-driven — agents must not invent facts
  - 🧩 Vendor agnostic and human-readable
  - ✅ Includes validation rules to keep generated context consistent
  - 📉 Helps reduce repeated repository analysis, token consumption, and context rediscovery
  
  > The core idea: **make project knowledge persistent so AI agents can spend more time solving problems and less time repeatedly understanding the repository.**
  
  </td>
  <td width="50%" valign="top">
  
  ### 🛒 [Supply Pilot](https://github.com/ElzioJunior/supply-pilot) 🔒
  
  An **AI-powered procurement platform** designed to coordinate supplier quotation workflows through conversational interfaces such as WhatsApp.
  
  The system turns unstructured buyer and supplier conversations into structured procurement state, allowing quotations to be collected, interpreted, compared, and presented to the buyer while keeping critical business decisions deterministic and auditable.
  
  **Highlights**
  
  - 💬 WhatsApp Business Platform integration with signed webhooks
  - 🧠 LLM-assisted interpretation of buyer and supplier natural-language messages
  - 📋 Structured outputs and strict validation around AI responses
  - 🏗️ Java + Spring Boot backend
  - 🗄️ PostgreSQL-backed quotation state and workflow persistence
  - 🔄 Supplier-specific quotation conversations
  - 📊 Deterministic comparison of usable commercial proposals
  - 👤 Human approval before supplier outreach and final purchasing decisions
  - 🔍 Progressive quotation status and summaries
  - 🧪 Unit, isolated functional, and real-provider integration test strategies
  
  AI is deliberately placed behind strict domain boundaries: the model helps **interpret language and structure information**, while business-critical eligibility, state transitions, proposal validation, and recommendation rules remain deterministic.
  
  > 🔒 **Private repository:** this project is currently private.  
  > The GitHub link will only work for users who have been explicitly added as collaborators.
  
  </td>
</tr>

<tr>
  <td width="50%" valign="top">

  ### 🏦 [Simplified Banking Service](https://github.com/ElzioJunior/simplified-banking-service)
  
  A **production-minded banking API** designed to manage accounts, transfers, and account movements with strong consistency, observability, and reliability guarantees.
  
  The system provides deterministic financial operations with idempotent transfers, concurrency control, asynchronous notifications, paginated movement history, and a complete local environment for running and observing the product.
  
  **Highlights**
  
  - 🏗️ Java + Spring Boot backend
  - 🗄️ PostgreSQL persistence with Flyway migrations
  - 💸 Atomic account-to-account transfers
  - 🔐 Idempotency protection for duplicate transfer requests
  - 🔒 Concurrency control and bounded database locks
  - 🐇 Asynchronous transfer notifications through RabbitMQ
  - 📄 Paginated account movements filtered by date range and credit/debit type
  - 📚 Swagger/OpenAPI documentation with request and validation examples
  - 📊 Prometheus metrics and preconfigured Grafana dashboards
  - ⚡ Gatling load and concurrency test scenarios
  - 🧪 Unit, isolated functional, and focused real-boundary integration tests
  - 🐳 Complete local environment provided through Docker Compose
  - 🤖 Engineering delivery supported by carefully designed agents, workflows, and skills
  - 📝 Architecture and business decisions documented through ADRs and BDRs
  
  Financial correctness remains deterministic: balance validation, transfer state changes, locking, idempotency, and transaction boundaries are enforced by the application and database. Asynchronous integrations are kept outside the financial transaction so external failures do not compromise committed banking operations.
  
  </td>
  
  <td width="50%" valign="top">

  ### 🚧 [RAG Pipeline for Software Projects](https://github.com/ElzioJunior/rag-pipeline-for-software-projects)
  
  > **STATUS: 🟡 TODO / DOING — under active design and construction**
  
  A language-agnostic **Retrieval-Augmented Generation pipeline for software repositories**.
  
  The project exists to explore how large software projects can be indexed so LLMs can retrieve precise, up-to-date code and architecture context instead of relying on oversized prompts or repeatedly scanning entire repositories.
  
  **Planned capabilities**
  
  - 🔎 Source-code repository traversal and parsing
  - ✂️ Semantic chunking of code and project metadata
  - 🧠 Embedding generation
  - 🗃️ Vector-based project indexing
  - 🔄 Incremental re-indexing as repositories evolve
  - 🌐 API layer for LLM context retrieval
  - ☕ Initial support focused on Java and Python
  
  > The objective is to create a reusable context-retrieval layer that lets AI systems query **the right project knowledge at the right time**, rather than loading the entire codebase into every interaction.
  
  </td>
</tr>

<tr>
  <td width="50%" valign="top">
  
  ### 🧵 [Virtual Threads Stress Test](https://github.com/ElzioJunior/virtual-threads-stress-test)
  
  A focused Java 21 experiment used as a **practical verification baseline for Virtual Threads under concurrent blocking workloads**.
  
  The project exposes equivalent blocking APIs backed by traditional platform threads and Java Virtual Threads, then drives both implementations through controlled load tests.
  
  **Highlights**
  
  - ☕ Java 21 + Spring Boot
  - 🧵 Platform Threads vs. Virtual Threads
  - 🚦 Controlled blocking workload
  - 📈 Gatling-based stress testing
  - ⚡ High-concurrency scenarios with thousands of simultaneous requests
  - 🔬 Designed to make the scalability characteristics of Virtual Threads easy to observe
  
  > The goal is not to claim a production benchmark, but to provide a reproducible environment for understanding how Virtual Threads behave when many concurrent operations spend most of their time waiting.
  
  </td>
  
  <td width="50%" valign="top">
  
  ### 📚 [Stacks New Features](https://github.com/ElzioJunior/stacks-new-features)
  
  A continuously evolving **technical knowledge repository used to stay current with the technologies I work with**.
  
  Instead of relying only on release notes, I keep concise references focused on the features and changes that matter most from an engineering perspective.
  
  Currently covering areas such as:
  
  - ☕ Java — from Java 8 through Java 25
  - 🐳 Docker — core concepts and major version changes
  - 📨 Apache Kafka — core concepts and evolution across releases
  
  The repository acts as a **personal engineering changelog**, making it easier to revisit important platform changes, compare versions, and keep technical knowledge fresh over time.
  
  </td>

</tr>
</table>

---

## 🧭 What I'm Exploring

```text
AI-assisted engineering
└── Agentic development, RAG, Structured outputs, Human + AI collaboration

Backend engineering
└── Java / Spring, Distributed systems, SQL/NoSQL, Cloud, Performance & observability
```

---

## 💡 Engineering Philosophy

> **AI should amplify engineering discipline, not replace it.**

I am especially interested in architectures where AI handles ambiguity — natural language, interpretation, summarization, and contextual reasoning — while deterministic software remains responsible for validation, state, business constraints, security, and critical decisions.

That separation makes AI-enabled systems easier to test, operate, audit, and evolve.

---

<div align="center">

### Building software, studying systems, and experimenting with what AI changes about engineering.

[![GitHub](https://img.shields.io/badge/GitHub-ElzioJunior-181717?style=for-the-badge&logo=github)](https://github.com/ElzioJunior)

</div>
