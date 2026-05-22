
# AI-Powered Microservice Debugging & RCA Platform

A production-grade multi-agent AI observability platform that autonomously analyzes logs, traces, metrics, and stack traces to identify root causes in distributed microservice systems.

Built using LangGraph orchestration, Gemini-powered reasoning agents, RAG pipelines, and Pinecone vector search.

---

# 🚀 Features

* Multi-agent AI workflow orchestration using LangGraph
* Parallel telemetry analysis agents
* RAG-powered observability intelligence
* Distributed trace correlation
* Root Cause Analysis (RCA) generation
* Structured outputs with Pydantic validation

---

# 🏗️ System Architecture

```text
Telemetry Input
(logs/traces/metrics)
        ↓
RAG Retrieval Layer
(Pinecone + Gemini Embeddings)
        ↓
LangGraph Orchestration
        ↓
Parallel Agents
 ├── Retrieval Agent
 ├── Log Analysis Agent
 ├── Trace Correlation Agent
 ├── Metrics Analysis Agent
 └── Stack Trace Agent
        ↓
Root Cause Agent
        ↓
RCA Report Generator
        ↓
FastAPI Response
```

---

# ⚙️ Tech Stack

| Layer           | Technology             |
| --------------- | ---------------------- |
| LLM             | Gemini 2.5 Flash       |
| AI Framework    | LangChain              |
| Orchestration   | LangGraph              |
| Vector Database | Pinecone               |
| Embeddings      | Gemini Embeddings      |
| Backend API     | FastAPI                |
| Cache           | Redis                  |
| Observability   | Prometheus + LangSmith |
| Deployment      | Docker + Kubernetes    |
| Validation      | Pydantic               |
| Async Runtime   | Python AsyncIO         |

---


# 🔄 Workflow Overview

## 1. Telemetry Ingestion

The platform ingests:

* application logs
* distributed traces
* metrics
* stack traces

---

## 2. RAG Retrieval

Relevant troubleshooting documents, telemetry logs, and KB articles are retrieved using:

* Gemini embeddings
* Pinecone vector search
* semantic similarity matching

---

## 3. Parallel Multi-Agent Analysis

LangGraph orchestrates parallel execution of specialized agents:

### Retrieval Agent

Fetches telemetry and KB context.

### Log Analysis Agent

Identifies:

* failures
* anomalies
* suspicious patterns

### Trace Correlation Agent

Detects:

* timeout propagation
* service dependency failures
* latency bottlenecks

### Metrics Analysis Agent

Analyzes:

* CPU spikes
* memory pressure
* high latency
* error rate anomalies

### Stack Trace Agent

Identifies:

* root exceptions
* failing components
* JVM/runtime failures

---

## 4. Root Cause Analysis

The Root Cause Agent correlates telemetry signals and determines:

* probable root cause
* impacted services
* severity
* blast radius
* remediation recommendations

---

## 5. RCA Report Generation

The system generates structured production-grade RCA reports including:

* incident summary
* root cause
* affected services
* failure propagation
* recommendations

---

# 🧠 Example RCA Output

```json
{
  "severity": "HIGH",
  "impacted_services": [
    "payment-service",
    "order-service"
  ],
  "probable_root_cause":
    "Database connection pool exhaustion",
  "failure_propagation":
    "payment-service → order-service → api-gateway",
  "recommendations": [
    "Increase DB pool size",
    "Optimize slow queries",
    "Add retry mechanisms"
  ]
}
```

---

