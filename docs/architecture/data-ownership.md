# Data Ownership Model

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Defines authoritative ownership of business data.

No service may directly write to another service's database.

Communication must occur through APIs or events.

---

# Identity Service

## Database

IdentityDB

## Owns

- Users
- Roles
- Permissions

---

# Customer Service

## Database

CustomerDB

## Owns

- Customers
- Addresses
- Preferences

---

# Policy Service

## Database

PolicyDB

## Owns

- Policies
- Coverage Information

---

# Claims Service

## Database

ClaimsDB

## Owns

- Claims
- Claim Status
- Claim History

---

# Document Service

## Database

DocumentDB

## Owns

- Document Metadata

## External Storage

- MinIO (Local)
- S3 (AWS)

---

# Fraud Service

## Database

FraudDB

## Owns

- Fraud Cases
- Fraud Scores

---

# AI Service

## Databases

AI Metadata DB

PostgreSQL + pgvector

## Owns

- Embeddings
- AI Assessments
- Prompt Templates

---

# Executive Insights Service

## Database

MetricsDB

## Owns

- KPIs
- ROI Metrics
- Cost Savings Metrics

---

# Data Ownership Rules

## Rule 1

Each service owns its own schema/database.

---

## Rule 2

Cross-service access occurs through:

- REST APIs
- Kafka Events

---

## Rule 3

No shared database tables.

---

## Rule 4

Events are the preferred integration mechanism.

---