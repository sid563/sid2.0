# 🚀 Scalable Order Management System (OMS v2)

A production-oriented **distributed order processing system** designed to handle high-throughput workloads with **fault tolerance, idempotency, and backpressure control**.

---

## 📌 Overview

This project simulates a real-world **Order Management System (OMS)** where:

* Orders are received via API
* Events are processed asynchronously using Kafka
* Consumers handle order creation with **idempotency guarantees**
* System is designed to handle **scaling, failures, and retries**

---

## 🏗️ Architecture

```
Client → API Service → Kafka → Consumer Service → Database
                         ↓
                      Retry / DLQ
```

---

## ⚙️ Tech Stack

* **Backend:** Node.js / TypeScript, Go, Rust (multi-service)
* **Message Queue:** Apache Kafka
* **Database:** MongoDB / PostgreSQL
* **Cache (optional):** Redis
* **Containerization:** Docker
* **Orchestration:** Kubernetes
* **Cloud:** AWS / GCP (optional deployment)

---

## 🔑 Key Features

### ✅ 1. Idempotent Order Processing

* Each order has a unique ID
* DB-level uniqueness ensures no duplicate orders
* Safe handling of Kafka re-delivery

---

### 🔁 2. Retry Mechanism + Dead Letter Queue (DLQ)

* Transient failures are retried with backoff
* Failed messages are pushed to DLQ for inspection

---

### ⚡ 3. Backpressure Handling

* Controlled consumer concurrency
* Prevents database overload
* Supports lag-based scaling

---

### 📈 4. Scalable Consumer System

* Horizontal scaling via Kubernetes
* Kafka lag-based auto-scaling (optional)

---

### 🧠 5. Failure-Aware Design

Handles:

* Consumer crashes
* Duplicate message delivery
* DB latency spikes
* Partial failures

---

### 📊 6. Monitoring & Alerts

* Metrics for:

  * Kafka lag
  * DB latency
  * Consumer throughput
* Alerting system (e.g., Telegram / Slack)

---

### 🤖 7. AI-based Log Analyzer (Optional)

* Uses LLM to:

  * Analyze logs
  * Suggest possible root causes
  * Improve debugging speed

---

## 🧪 System Design Considerations

### 🔹 Idempotency Strategy

* Unique constraint on order ID
* Safe retry handling

### 🔹 Consistency vs Availability

* Eventual consistency using async processing

### 🔹 Scaling Strategy

* Kafka handles ingestion
* Consumers scale horizontally
* DB protected via throttling

### 🔹 Failure Handling

* Retry with exponential backoff
* DLQ for poison messages

---

## 🚀 Getting Started

### Prerequisites

* Docker
* Kafka
* Node.js / Go / Rust
* MongoDB / PostgreSQL

---

### Run Locally

```bash
# Clone repo
git clone https://github.com/your-username/oms-v2.git

# Start services
docker-compose up

# Start API service
cd api-service && npm install && npm run dev

# Start consumer
cd consumer-service && npm install && npm run dev
```

---

## 📂 Project Structure

```
oms-v2/
│
├── api-service/          # Receives orders and produces events
├── consumer-service/    # Processes orders
├── common/              # Shared utilities (ID generator, configs)
├── infra/               # Docker, Kubernetes configs
├── docs/                # Architecture and design docs
```

---

## 📌 Future Improvements

* Distributed ID generation (Snowflake)
* Rate limiting at API level
* Advanced monitoring dashboards (Prometheus + Grafana)
* Multi-region deployment
* Exactly-once semantics (advanced Kafka setup)

---

## 🧠 Learnings

This project focuses on:

* Real-world distributed system challenges
* Designing for failures, not just success cases
* Understanding trade-offs in scalability and consistency

---

## 👨‍💻 Author

Siddharth Singh
Backend Engineer | Distributed Systems Enthusiast

---

## ⭐ Final Note

> This project is not just about building a system
> It’s about understanding how systems behave under load, failure, and scale

---
