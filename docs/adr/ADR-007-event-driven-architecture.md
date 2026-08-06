# ADR-007: Adopt Event-Driven Architecture

## Status

Accepted

## Date

July 2026

---

# Context

CloudSure consists of independently deployed business services.

Direct synchronous communication between all services would create tight coupling.

---

# Decision

The platform shall adopt an event-driven architecture using Kafka.

---

# Key Events

Examples:

- CustomerRegistered
- PolicyCreated
- ClaimCreated
- ClaimApproved
- FraudDetected
- AIAnalysisCompleted

---

# Rationale

Benefits:

- Loose coupling
- Scalability
- Resilience
- Asynchronous processing

---

# Integration Style

Primary:

- Kafka Events

Secondary:

- REST APIs

---

# Consequences

Positive:

- Better scalability
- Independent service evolution

Negative:

- Eventual consistency
- Increased observability requirements

---