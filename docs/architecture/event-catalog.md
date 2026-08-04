# Event Catalog

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Defines all business events published through Kafka.

These events form the backbone of the event-driven architecture.

---

# CustomerRegistered

## Producer

Customer Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

Customer account created.

---

# PolicyCreated

## Producer

Policy Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

New policy issued.

---

# PolicyRenewed

## Producer

Policy Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

Policy renewed.

---

# ClaimCreated

## Producer

Claims Service

## Consumers

- AI Service
- Fraud Service
- Notification Service
- Executive Insights Service

## Purpose

New claim submitted.

---

# ClaimUpdated

## Producer

Claims Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

Claim status changed.

---

# ClaimApproved

## Producer

Claims Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

Claim approved.

---

# ClaimRejected

## Producer

Claims Service

## Consumers

- Notification Service
- Executive Insights Service

## Purpose

Claim rejected.

---

# DocumentUploaded

## Producer

Document Service

## Consumers

- AI Service
- Claims Service

## Purpose

Claim document uploaded.

---

# FraudDetected

## Producer

Fraud Service

## Consumers

- Claims Service
- Executive Insights Service

## Purpose

Potential fraud identified.

---

# AIAnalysisCompleted

## Producer

AI Service

## Consumers

- Claims Service
- Executive Insights Service

## Purpose

AI recommendation generated.

---

# CostSavingsCalculated

## Producer

Executive Insights Service

## Consumers

- Executive Dashboard

## Purpose

AI savings metrics updated.

---

# Event Naming Convention

All events follow:

```text
<Entity><Action>
```

Examples:

```text
ClaimCreated

ClaimApproved

PolicyRenewed

FraudDetected
```

---

# Event Design Principles

1. Events represent facts.

2. Events are immutable.

3. Events contain business meaning.

4. Events support eventual consistency.

5. Events are versioned when schema changes occur.

---