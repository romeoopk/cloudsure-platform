# C4 Container Diagram

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Defines the major deployable runtime containers within CloudSure.

---

# Containers

## Identity Service

Responsible for:

- Authentication
- Authorization

Database:

IdentityDB

---

## Customer Service

Responsible for:

- Customer Profiles

Database:

CustomerDB

---

## Policy Service

Responsible for:

- Policies
- Quotes

Database:

PolicyDB

---

## Claims Service

Responsible for:

- Claim Submission
- Claim Tracking

Database:

ClaimsDB

---

## Document Service

Responsible for:

- Document Storage

Database:

DocumentDB

Storage:

MinIO / S3

---

## Fraud Service

Responsible for:

- Fraud Detection

Database:

FraudDB

---

## AI Service

Responsible for:

- Insurance Copilot
- Claims Agent
- RAG

Database:

PostgreSQL + pgvector

---

## Executive Insights Service

Responsible for:

- KPIs
- Savings Tracking
- ROI

Database:

MetricsDB

---

## Notification Service

Responsible for:

- Email
- SMS

---

# Shared Platform Components

## Kafka

Event Backbone

---

## Redis

Caching

---

## PostgreSQL

Transactional Data

---

## MongoDB

Audit Data
Metadata
AI Interactions

---

# Logical View

```text
Customer

     |

 API Gateway

     |

---------------------------------------------------

Identity Service

Customer Service

Policy Service

Claims Service

Document Service

Fraud Service

AI Service

Executive Insights Service

Notification Service

---------------------------------------------------

Kafka
Redis

PostgreSQL

MongoDB

pgvector
```

---