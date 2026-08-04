# Saga Patterns

**Project:** CloudSure - AI Native Insurance Platform

**Version:** 1.0

---

# Purpose

CloudSure follows an event-driven microservices architecture.

Because each service owns its own database, traditional distributed database transactions are not possible.

CloudSure uses the Saga Pattern to coordinate business processes across services.

---

# Why Sagas?

Traditional Monolith

```text
BEGIN TRANSACTION

Update Claim
Update Policy
Update Payment

COMMIT
```

Microservices

```text
Claims DB

Policy DB

Fraud DB

AI DB
```

No shared transaction exists.

Sagas provide eventual consistency.

---

# Saga Style

CloudSure primarily adopts:

```text
Choreography-Based Sagas
```

using:

```text
Kafka Events
```

---

# Claim Processing Saga

## Business Goal

Process a submitted insurance claim.

---

# Happy Path

```text
Claim Created

      |

ClaimCreated Event

      |

AI Analysis

      |

Fraud Analysis

      |

Adjuster Review

      |

Claim Approved

      |

Notification Sent

      |

Executive Metrics Updated
```

---

# Service Participation

## Claims Service

Creates Claim.

Produces:

```text
ClaimCreated
```

---

## AI Service

Consumes:

```text
ClaimCreated
```

Produces:

```text
AIAnalysisCompleted
```

---

## Fraud Service

Consumes:

```text
ClaimCreated
```

Produces:

```text
FraudDetected
```

or

```text
FraudCheckCompleted
```

---

## Claims Adjuster

Reviews recommendations.

Produces:

```text
ClaimApproved

ClaimRejected
```

---

## Notification Service

Informs customer.

---

## Executive Insights Service

Tracks metrics and savings.

---

# Compensation Logic

Unlike traditional rollback, CloudSure uses business compensation.

---

## Example

Claim approved incorrectly.

Compensation actions:

```text
Open Investigation

Suspend Payment

Create Fraud Case
```

---

## Example

AI Analysis Failed.

Compensation:

```text
Manual Review Required
```

---

## Example

Notification Failure.

Compensation:

```text
Retry Notification

Dead Letter Queue
```

---

# Policy Creation Saga

## Happy Path

```text
Customer Requests Policy

      |

Quote Generated

      |

Policy Created

      |

PolicyCreated Event

      |

Customer Notified

      |

Executive Metrics Updated
```

---

# Executive Metrics Saga

## Goal

Keep executive dashboards synchronized.

---

Events Consumed

```text
PolicyCreated

ClaimCreated

ClaimApproved

ClaimRejected

FraudDetected

AIAnalysisCompleted
```

---

Metrics Calculated

```text
Claims Processed

Hours Saved

Cost Savings

Fraud Prevention

AI Adoption
```

---

# Dead Letter Strategy

Failed events move to:

```text
Dead Letter Topics
```

Examples:

```text
claim-created-dlt

policy-created-dlt
```

---

# Idempotency

All consumers must support:

```text
At-Least-Once Delivery
```

Consumers shall be idempotent.

---

Example:

```text
Same event processed twice

Result remains identical
```

---

# Eventual Consistency

CloudSure accepts:

```text
Temporary Data Inconsistency
```

while guaranteeing:

```text
Eventual Consistency
```

across all business services.

---

# Future Roadmap

Potential enhancements:

```text
Saga Orchestrator

Temporal

Camunda

Conductor
```

for long-running workflows.

---
``