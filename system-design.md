# 🏗️ System Design Question Bank (Backend Engineer)

## 🎯 Goal

* Build strong system design thinking
* Prepare for backend + distributed system interviews
* Learn to design **scalable, fault-tolerant systems**

---

# 📅 How to Use This Sheet

For each question:

1. Define requirements (functional + non-functional)
2. Estimate scale (users, QPS, data size)
3. Design high-level architecture
4. Identify bottlenecks
5. Discuss trade-offs
6. Add failure handling

---

# 🟢 LEVEL 1 — CORE SYSTEMS (Must Do)

## 🔹 1. Design URL Shortener (like bit.ly)

Focus:

* Hashing
* DB schema
* Read-heavy optimization
* Caching

---

## 🔹 2. Design Rate Limiter

Focus:

* Token bucket / leaky bucket
* Redis usage
* Distributed rate limiting

---

## 🔹 3. Design Notification System

Focus:

* Queue-based processing
* Retry logic
* Multi-channel delivery (email, SMS)

---

## 🔹 4. Design Logging System

Focus:

* High write throughput
* Log aggregation
* Storage strategy

---

## 🔹 5. Design File Upload System (like Google Drive)

Focus:

* Chunk uploads
* Storage (S3)
* Metadata DB

---

# 🟡 LEVEL 2 — BACKEND HEAVY SYSTEMS

## 🔹 6. Design Order Management System (OMS)

Focus:

* Kafka
* Idempotency
* Transactions
* Retry + DLQ
* Backpressure

---

## 🔹 7. Design Payment System

Focus:

* Consistency
* Idempotency
* Failure handling
* External APIs

---

## 🔹 8. Design Inventory Management System

Focus:

* Concurrency issues
* Race conditions
* Locking strategies

---

## 🔹 9. Design Chat System (like WhatsApp)

Focus:

* Real-time messaging
* WebSockets
* Message ordering

---

## 🔹 10. Design Email Service

Focus:

* Queueing
* Retry
* Spam handling

---

# 🔵 LEVEL 3 — SCALING & DISTRIBUTED SYSTEMS

## 🔹 11. Design News Feed (like Facebook)

Focus:

* Fan-out vs pull model
* Caching
* Ranking

---

## 🔹 12. Design Search System

Focus:

* Indexing
* Query optimization
* ElasticSearch basics

---

## 🔹 13. Design Ride Sharing (like Uber)

Focus:

* Location tracking
* Matching algorithm
* Real-time updates

---

## 🔹 14. Design Video Streaming (like YouTube)

Focus:

* CDN
* Chunk streaming
* Storage

---

## 🔹 15. Design Distributed Cache

Focus:

* Cache invalidation
* Consistency
* Eviction policies

---

# 🔴 LEVEL 4 — ADVANCED (High Paying Roles)

## 🔹 16. Design Event Streaming System (Kafka-like)

Focus:

* Partitioning
* Replication
* Fault tolerance

---

## 🔹 17. Design Multi-Tenant SaaS System

Focus:

* Isolation
* Scaling
* Data partitioning

---

## 🔹 18. Design Global ID Generator (Snowflake)

Focus:

* Distributed uniqueness
* Ordering
* Clock issues

---

## 🔹 19. Design Real-Time Analytics System

Focus:

* Stream processing
* Aggregation
* Storage layers

---

## 🔹 20. Design Fault-Tolerant Job Scheduler

Focus:

* Retry
* Scheduling
* Distributed workers

---

# 🧠 MUST-KNOW DESIGN CONCEPTS

## 🔹 Scalability

* Horizontal vs Vertical scaling
* Load balancing

## 🔹 Data Management

* SQL vs NoSQL
* Sharding
* Replication

## 🔹 Caching

* Redis
* Cache invalidation strategies

## 🔹 Messaging Systems

* Kafka
* At-least-once vs exactly-once

## 🔹 Reliability

* Retry strategies
* Circuit breaker
* Idempotency

## 🔹 Backpressure

* Rate limiting
* Queue control
* Consumer throttling

---

# 🔁 PRACTICE STRATEGY

### Week Plan:

* Week 1–2 → Level 1
* Week 3–4 → Level 2
* Week 5–6 → Level 3
* Week 7+ → Advanced topics

---

# 🧪 MOCK INTERVIEW PREP

Practice:

* Explaining architecture clearly
* Thinking aloud
* Handling follow-up questions:

  * “What if this fails?”
  * “How will it scale?”
  * “What are trade-offs?”

---

# ⚠️ COMMON MISTAKES

❌ Jumping to tools (Kafka, Redis) without need
❌ Ignoring scale estimation
❌ No failure handling
❌ Overengineering

---

# 🚀 FINAL TARGET

After completing this sheet:

You should be able to:

* Design scalable backend systems
* Handle edge cases
* Explain trade-offs confidently

---

# 🧠 FINAL PRINCIPLE

> Good engineers design systems that work
> Great engineers design systems that survive failure

---
