# C4 System Context Diagram

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Provides a high-level view of the CloudSure platform and its interactions with users and external systems.

---

# Actors

## Customer

Uses:

- Policy Management
- Claims Submission
- Insurance Copilot

---

## Insurance Agent

Uses:

- Customer Management
- Policy Services

---

## Claims Adjuster

Uses:

- Claims Service
- Fraud Analysis
- AI Recommendations

---

## Operations Manager

Uses:

- Operations Dashboard

---

## Executive

Uses:

- Executive Dashboard
- ROI Analytics

---

# External Systems

## Ollama

Provides:

- LLM Inference
- Embeddings

---

## Email Provider

Provides:

- Outbound Notifications

---

## AWS

Provides:

- Kubernetes Platform
- Storage
- Managed Databases

---

# Context Diagram

```text
+--------------------+
|     Customers      |
+--------------------+
          |
          v

+--------------------------------+
|          CloudSure             |
| AI Native Insurance Platform   |
+--------------------------------+
     |      |      |      |
     |      |      |      |
     v      v      v      v

 Ollama   Email   AWS   Future Integrations
```

---

# Business Outcomes

CloudSure provides:

- Insurance Management
- Claims Processing
- Fraud Detection
- AI Assistance
- Executive Intelligence

---