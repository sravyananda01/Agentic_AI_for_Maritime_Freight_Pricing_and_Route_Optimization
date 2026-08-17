# 🚢 FreightQuote AI
## Agentic AI for Maritime Freight Pricing and Route Optimization

**Infosys Springboard Internship — Milestone 4**  
**Codename:** FreightQuote AI

---

## 📌 Project Overview

FreightQuote AI is an agentic decision-support platform for an ocean-freight brokerage.

The platform monitors global and Indian ports, calculates dynamic freight quotes, benchmarks carriers, tracks weather and customs risk, generates shipping documents, supports multilingual freight information, and provides an LLM-powered AI Copilot.

Milestone 4 integrates the work completed in **Milestones 1, 2 and 3** into one complete Overall Execution Application.

The final platform combines:

- 🤖 AI Copilot
- 🗺️ Route Intelligence
- 💰 Dynamic Freight Pricing
- 🏢 Carrier Performance & Capacity Intelligence
- 🌩️ Weather Risk & Storm Telemetry
- 📈 Margin Prediction & Yield Optimization
- 📜 Customs, Tariff & Regulatory Intelligence
- 📄 Digital Bill of Lading & OCR
- 🌐 Freight Document Translation
- 📚 Custom PDF RAG
- 🚨 Alerts & Incidents
- 🔔 Notifications
- 🕸️ Knowledge Graph
- ⚡ Digital Twin
- 🚨 Anomaly/Risk Scanner
- 📡 Data Feed Center
- 🛡️ Admin Dashboard
- 🔐 Authentication and RBAC

---

# 🆕 What Milestone 4 Adds on Top of Milestones 1, 2 and 3

## Milestone 1 — Authentication & Security

Milestone 1 provides the secure authentication foundation:

- Signup
- Login
- OTP verification
- Security Question
- Security Answer
- OTP-based password recovery
- Security-question password recovery
- Password hashing
- JWT/session handling
- Logout
- Role-Based Access Control
- Account protection

---

## Milestone 2 — Freight Intelligence

Milestone 2 provides the core maritime intelligence capabilities:

- Route intelligence
- Freight pricing
- Carrier performance
- Weather risk
- Freight margin analysis
- Customs intelligence
- AI-based analysis
- Operational freight database

---

## Milestone 3 — RAG & Document Intelligence

Milestone 3 introduces document-grounded AI:

- PDF processing
- Text extraction
- Text chunking
- Sentence embeddings
- FAISS vector indexing
- Semantic retrieval
- Document-based question answering
- Maritime document knowledge base
- RAG integration

---

## Milestone 4 — Overall Integration

Milestone 4 brings the previous milestone functionality together and adds:

- Complete integrated Streamlit application
- RAG Engine integration
- Kaggle DataPipeline integration
- Nine specialized maritime agents
- Grounded AI Copilot
- Multilingual AI support
- Digital Bill of Lading
- OCR
- Alerts and incident management
- Notifications
- Knowledge Graph
- Digital Twin
- Anomaly/Risk Scanner
- Data Feed Center
- Extended Admin Dashboard
- Indian port coverage

---

# 🏗️ System Architecture

```text
                              👤 USER
                                │
                                ▼
                    ┌────────────────────────┐
                    │ AUTHENTICATION & RBAC   │
                    │ Signup / Login / OTP   │
                    │ Security Questions      │
                    │ JWT / Session / Logout  │
                    └────────────┬───────────┘
                                 │
                                 ▼
                    ┌────────────────────────┐
                    │      STREAMLIT APP      │
                    │      FreightQuote AI    │
                    └────────────┬───────────┘
                                 │
             ┌───────────────────┼────────────────────┐
             │                   │                    │
             ▼                   ▼                    ▼
       🤖 AI COPILOT        ⚙️ AI AGENTS          🛡️ ADMIN
             │                   │                    │
             │        ┌──────────┼───────────┐        │
             │        │          │           │        │
             │        ▼          ▼           ▼        │
             │      Route      Pricing     Carrier    │
             │      Weather    Margin      Customs    │
             │      OCR        Translation             │
             │                                         │
             └────────────────┬────────────────────────┘
                              │
                  ┌───────────┴───────────┐
                  │                       │
                  ▼                       ▼
             📚 RAG ENGINE          📊 DATA PIPELINE
                  │                       │
                  ▼                       ▼
             PDF Documents          Kaggle Dataset
                  │                       │
                  ▼                       ▼
             Text Chunking           Data Cleaning
                  │                       │
                  ▼                       ▼
             Embeddings              Transformation
                  │                       │
                  ▼                       ▼
             FAISS Vector DB         Validated Data
                  │                       │
                  └───────────┬───────────┘
                              │
                              ▼
                       🗄️ SQLITE DATABASE
                              │
                              ▼
                       GROUNDED RESULTS
