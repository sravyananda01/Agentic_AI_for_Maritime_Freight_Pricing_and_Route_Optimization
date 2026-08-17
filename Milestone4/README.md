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


---

🔄 Milestone 4 Execution Workflow

The mandatory execution order is:

STEP 01
RAG ENGINE
    │
    ▼
STEP 02
KAGGLE DATAPIPELINE
    │
    ▼
STEP 03
OVERALL APPLICATION
    │
    ▼
AI COPILOT + AGENTS + PLATFORM FEATURES


---

🤖 AI COPILOT

Purpose

The AI Copilot is the natural-language assistant of the FreightQuote AI platform.

It answers questions related to:

Shipments

Pricing

Routes

Weather

Customs

Carriers

Maritime documents


Working

User Question
      │
      ▼
Intent Classification
      │
      ▼
Grounded Query
      │
      ├──────── SQL / Database Facts
      │
      ├──────── Route Solver
      │
      ├──────── Freight Quote Calculator
      │
      └──────── RAG Retrieval
                       │
                       ▼
                Retrieved Context
                       │
                       ▼
                 Qwen LLM
                       │
                       ▼
              Grounded Answer
                       │
                       ▼
              Optional Translation

AI Copilot Quality

The Copilot is designed to be:

Multilingual

Grounded

Creative


It can provide:

What-if scenarios

Alternative strategies

Actionable recommendations

Intelligent summaries

Business ideas


The Copilot should not fabricate facts, numbers or sources.

When evidence is unavailable, it should clearly state that the information is unavailable.


---

⚙️ AGENT 1 — Global Ocean Port & Route Intelligence

Purpose

Provides port telemetry and maritime route intelligence across monitored global and Indian ports.

Key Features

🗺️ Live interactive port network map

Port congestion monitoring

Active vessel information

Dynamic route optimizer

Port-to-port distance calculation

Sailing-time estimation

Route and port risk classification

AI Route Advisor

Maritime fuel-efficiency analysis


Working

Origin Port + Destination Port
              │
              ▼
     Haversine Distance
              │
              ▼
      Sailing-Time Estimate
              │
              ▼
       Route Risk Analysis
              │
              ▼
      Route Recommendation

ML Models

RandomForest

GradientBoosting

DecisionTree

LogisticRegression

SVC


Charts

Folium Map

Bar Chart

Scatter Plot


Chart Interpretation

On the port map:

Green = lower congestion

Orange = medium congestion

Red/darker red = higher congestion


Higher congestion indicates greater expected dwell time.


---

💰 AGENT 2 — Dynamic Freight Pricing & Rate Calculator

Purpose

Calculates and benchmarks ocean freight quotes.

Key Features

From-to freight rate calculator

Base ocean rate

Fuel surcharge

Customs/terminal handling fee

Final freight price

Multi-model freight-pricing benchmark

Waterfall cost analysis

Correlation heatmap

Quote-value funnel

AI Pricing Advisor


Working

Base Ocean Rate
       │
       ▼
Fuel Surcharge
       │
       ▼
Customs / Terminal Fee
       │
       ▼
Final Freight Price

ML Models

RandomForestRegressor

GradientBoostingRegressor

DecisionTreeRegressor

LinearRegression


Charts

Waterfall

Heatmap

Funnel

Bar Chart


Chart Interpretation

The waterfall chart shows how the final quote is built:

Base Cost
   +
Fuel
   +
Fees
   =
Final Price


---

🏢 AGENT 3 — Carrier Performance & Safety Audit

Purpose

Benchmarks shipping carriers based on safety, reliability and fleet capacity.

Key Features

Carrier reliability analysis

Safety analysis

Fleet capacity analysis

8-parameter capacity simulator

Carrier comparison

Risk analysis

AI Carrier Advisor


Working

Carrier Data
     │
     ▼
Performance Analysis
     │
     ▼
Reliability + Safety + Capacity
     │
     ▼
Risk Evaluation
     │
     ▼
Carrier Recommendation

ML Models

RandomForestClassifier

GradientBoostingClassifier

DecisionTreeClassifier

LogisticRegression

SVC


Charts

Treemap

Scatter Plot

Heatmap

Radar


Chart Interpretation

In the treemap:

Larger rectangle = larger fleet contribution

High-risk branches require more attention

Low-rated high-risk carriers should be reviewed first


In the scatter plot:

Higher rating + higher on-time percentage = more dependable carrier



---

🌩️ AGENT 4 — Global Weather Risk & Harbor Safety Intelligence

Purpose

Monitors severe weather and storm risk at monitored ports.

Key Features

🗺️ Live storm-severity port map

Weather monitoring

Storm risk analysis

Harbor safety analysis

Wind-speed analysis

Wave-height analysis

Weather-risk prediction

AI Weather Advisor


Working

Port Coordinates
      │
      ▼
Live Weather Data
      │
      ▼
Weather Risk Analysis
      │
      ▼
Safety Classification
      │
      ▼
Weather Recommendation

Live Weather

The platform uses the Open-Meteo REST API through the weather context layer.

ML Models

RandomForest

GradientBoosting

DecisionTree

LogisticRegression

SVC

LinearRegression


Charts

Folium Map

Bar Chart

Scatter Plot


Chart Interpretation

In the wind-speed vs wave-height chart:

Points within the safety range indicate lower risk.

Points beyond the safety threshold indicate higher harbor risk.

High-risk ports may require anchorage or rerouting.



---

📈 AGENT 5 — Freight Margin Optimizer & Profitability Intelligence

Purpose

Analyzes where freight margin is earned or lost.

Key Features

10-parameter rate simulator

Carrier yield matrix

Freight margin prediction

Cost analysis

Profitability analysis

Margin optimization

AI Margin Advisor


Working

Freight Revenue
      │
      ▼
Cost Components
      │
      ▼
Margin Calculation
      │
      ▼
Profitability Analysis
      │
      ▼
Yield Recommendation

ML Models

RandomForestRegressor

GradientBoostingRegressor

DecisionTreeRegressor

LinearRegression


Charts

Box Plot

Heatmap

Histogram


Chart Interpretation

A carrier with a low median margin and repeated low-margin deals may require renegotiation.

A strong negative relationship between fuel surcharge and margin indicates fuel volatility as a major margin risk.


---

📜 AGENT 6 — Customs Intelligence & HS Code Compliance

Purpose

Assesses regulatory clearance risk based on country and cargo type.

Key Features

Customs intelligence

HS Code compliance

Customs duty simulator

Regulatory document matrix

Clearance-risk analysis

Duty exposure analysis

AI Customs Advisor


Working

Cargo Type
     │
     ▼
HS Code + Origin Country
     │
     ▼
Customs / Duty Analysis
     │
     ▼
Clearance Risk
     │
     ▼
Compliance Recommendation

ML Models

RandomForestClassifier

GradientBoostingClassifier

DecisionTreeClassifier

LogisticRegression

SVC


Charts

Sunburst

Scatter Plot


Chart Interpretation

Sunburst:

Inner Ring = Origin Country
Outer Ring = Cargo Type

Red-toned areas indicate higher clearance risk.

In the duty-vs-risk scatter:

High duty + high risk = lanes requiring greater attention



---

📄 AGENT 7 — Quote Document & Bill of Lading Generator

Purpose

Produces shipping documents from live freight quote information.

Key Features

Freight quote PDF

Bill of Lading generation

Shipping document generation

OCR/document processing


Working

Live Quote Data
      │
      ▼
Document Generation
      │
      ├── Freight Quote PDF
      │
      └── Bill of Lading

Technologies

Python

PDF processing

ReportLab / FPDF

OCR



---

🌐 AGENT 8 — Freight Document & Policy Translation Engine

Purpose

Provides multilingual translation for freight documents and policies.

Key Features

Real-time text translation

Maritime document translation

Batch translation

Maritime trade glossary

BAF terminology

TEU terminology

HS Code terminology

Dwell-time terminology

Supported languages


Working

Freight Text / Document
          │
          ▼
    Translation Engine
          │
          ▼
     Target Language

Technology

Facebook NLLB-200

Distilled 600M model

NLP

Transformers



---

📚 AGENT 9 — Custom PDF Knowledge Base & Vector RAG Engine

Purpose

Provides a custom RAG workbench for maritime PDF documents.

Supported document types include:

Customs manuals

Carrier SOPs

Contracts

Maritime policies


Working

Upload PDF
    │
    ▼
Text Extraction
    │
    ▼
Text Chunking
    │
    ▼
Sentence Embeddings
    │
    ▼
FAISS Vector Index
    │
    ▼
User Question
    │
    ▼
Similarity Search
    │
    ▼
Relevant Document Chunks
    │
    ▼
LLM
    │
    ▼
Grounded Answer

Technologies

PDF processing

LangChain text splitters

Sentence Transformers

FAISS

Qwen LLM



---

🚨 NOTIFICATIONS — Unified Incident & Alert Center

Purpose

Provides one centralized place for operational alerts and incidents.

Key Features

Live incident feed

Shipment delay alerts

Weather hold alerts

Customs issue alerts

Severity information

One-click incident resolution


Visualization

Pie Chart for severity breakdown



---

🕸️ KNOWLEDGE GRAPH

Purpose

Represents relationships between maritime entities.

Example

PORT
                   │
          ┌────────┴────────┐
          │                 │
        ROUTE           WEATHER
          │
       SHIPMENT
          │
       CARRIER

Main Relationships

Port ↔ Route

Route ↔ Shipment

Shipment ↔ Carrier

Port ↔ Weather



---

⚡ DIGITAL TWIN

Purpose

Provides a digital representation of the maritime freight network.

Uses

Network simulation

Operational analysis

Scenario analysis

Decision support


Working

Real Maritime Network
          │
          ▼
      Digital Twin
          │
          ▼
       Simulation
          │
          ▼
    Decision Support


---

🚨 ANOMALY / RISK SCANNER

Purpose

Detects unusual patterns and potential operational risks.

Examples

Shipment anomalies

Freight-value anomalies

Port anomalies

Operational outliers

Network-level risks


Working

Operational Data
      │
      ▼
Anomaly Detection
      │
      ▼
Normal / Abnormal
      │
      ▼
Risk Identification
      │
      ▼
Alert / Investigation


---

📡 DATA FEED CENTER

Purpose

Provides raw and operational data for review and application use.

Working

Kaggle / Operational Data
          │
          ▼
      Data Pipeline
          │
          ▼
Data Cleaning / Processing
          │
          ▼
      Application Data
          │
          ▼
        AI Agents

Features

Raw operational data review

Data access

Data export/review

Application data availability



---

🛡️ ADMIN DASHBOARD

Purpose

Provides administration and system monitoring.

User Management

Add users

Delete users

Promote users

Demote users

Unlock users

Assign roles


System Health

Database status

LLM status

Translation engine status


ML Performance

The application can maintain a model-performance ledger containing:

Accuracy

F1

R²


Audit

Chat history

User activity

Audit trail



---

🔐 ROLE-BASED ACCESS CONTROL

Role	Access

Admin	All tabs including Admin Dashboard
Freight Broker / Regional Ops Manager	All agents and AI Copilot except Admin Dashboard
Dispatcher	AI Copilot and selected operational agents
Customer / Client	AI Copilot and quote-related agents



---

🇮🇳 INDIAN PORT COVERAGE

Port	State	Coverage / Usage

🇮🇳 Mumbai (JNPT)	Maharashtra	Port, route, freight and operational analysis
🇮🇳 Mundra	Gujarat	Port, route, freight and operational analysis
🇮🇳 Chennai	Tamil Nadu	Port, route, freight and operational analysis
🇮🇳 Cochin	Kerala	Port, route, freight and operational analysis


These ports provide localized Indian maritime coverage for the application's route, freight, weather and operational intelligence.


---

📊 KAGGLE DATA PIPELINE

Purpose

The Kaggle DataPipeline prepares freight-related data before it is used by the Overall Application.

Pipeline

Kaggle Dataset
      │
      ▼
Data Loading
      │
      ▼
Data Cleaning
      │
      ▼
Data Transformation
      │
      ▼
Data Validation
      │
      ▼
Application Data
      │
      ▼
SQLite / AI Agents


---

📚 RAG ENGINE

Purpose

The RAG Engine provides document-grounded knowledge to the application.

Pipeline

Maritime Documents
       │
       ▼
PDF Processing
       │
       ▼
Text Extraction
       │
       ▼
Chunking
       │
       ▼
Embeddings
       │
       ▼
FAISS Vector Store
       │
       ▼
User Question
       │
       ▼
Relevant Context
       │
       ▼
LLM
       │
       ▼
Grounded Answer


---

🧠 MACHINE LEARNING

Different agents benchmark classical ML models for their prediction tasks.

Classification

Used for:

Carrier reliability

Weather risk

Customs clearance risk


Models:

Random Forest

Gradient Boosting

Decision Tree

Logistic Regression

SVC


Metrics:

Accuracy

F1 Score


Regression

Used for:

Freight pricing

Freight margin


Models:

Random Forest Regressor

Gradient Boosting Regressor

Decision Tree Regressor

Linear Regression


Metrics:

R²

RMSE



---

📊 VISUALIZATION

Chart Type	Purpose

Bar Chart	Compare values between categories
Scatter Plot	Show relationship between numeric variables
Box Plot	Show median, quartiles and outliers
Histogram	Show data distribution
Sunburst	Show hierarchical data
Treemap	Show hierarchical proportions
Waterfall	Show sequential additions/subtractions
Funnel	Show sequential pipeline stages
Heatmap	Show relationships/correlations
Folium Map	Show geographic information
Radar	Compare multiple carrier parameters



---

🛠️ TECHNOLOGY STACK

Layer	Technology	Purpose

Frontend	Streamlit	Web application
Navigation	streamlit-option-menu	Application navigation
Backend	Python	Application and agent logic
Database	SQLite	Operational freight data
LLM	Qwen2.5-3B-Instruct	Natural-language reasoning
Fallback LLM	Qwen2.5-1.5B-Instruct	Fail-soft model
RAG	FAISS	Vector search
Embeddings	Sentence Transformers	Document embeddings
Text Splitting	LangChain	Document chunking
Translation	NLLB-200	Multilingual translation
ML	Scikit-learn	Prediction and classification
Visualization	Plotly	Interactive analytics
Maps	Folium	Port and weather maps
Weather	Open-Meteo REST API	Live weather
Authentication	PyJWT	JWT authentication
Password Security	bcrypt	Password hashing
Documents	ReportLab / FPDF	PDF generation
Data	Kaggle / Faker	Data generation and seeding
Runtime	Google Colab	Development environment
Tunnel	ngrok / Cloudflare Tunnel	Public application URL
Version Control	Git / GitHub	Repository management



---

🔑 GOOGLE COLAB SECRETS SETUP

Sensitive credentials must not be hard-coded into notebooks.

Step 1 — Open Colab

Open the required notebook in Google Colab.

Step 2 — Open Secrets

Click the 🔑 Secrets icon in the left sidebar.

Step 3 — Add Secret

Click:

Add new secret

Enter the required:

Secret Name
Secr
