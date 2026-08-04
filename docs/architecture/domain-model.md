# Domain Model

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

This document defines the core business entities, their relationships, and ownership within the CloudSure platform.

The domain model serves as the foundation for:

- Microservice decomposition
- Database design
- API design
- Event design
- Domain-driven design (DDD)

---

# Core Domains

## Customer

Represents a registered insurance customer.

### Attributes

- CustomerId
- FirstName
- LastName
- DateOfBirth
- Email
- Phone
- Address
- Status

### Relationships

- Customer owns Policies
- Customer submits Claims

---

## Policy

Represents an active insurance contract.

### Attributes

- PolicyId
- PolicyNumber
- PolicyType
- EffectiveDate
- ExpirationDate
- Premium
- CoverageAmount
- Status

### Policy Types

- Auto
- Home
- Life

### Relationships

- Policy belongs to Customer
- Policy contains Claims

---

## Claim

Represents a request for compensation.

### Attributes

- ClaimId
- ClaimNumber
- ClaimType
- ClaimStatus
- SubmittedDate
- Description

### Status

- Submitted
- UnderReview
- Approved
- Rejected
- Settled

### Relationships

- Claim belongs to Policy
- Claim contains Documents
- Claim receives AI Assessments

---

## Document

Represents uploaded content.

### Attributes

- DocumentId
- FileName
- FileType
- UploadDate
- StorageLocation

### Types

- Policy Document
- Claim Photo
- Police Report
- Repair Estimate

### Relationships

- Document belongs to Claim

---

## Fraud Case

Represents fraud investigation activities.

### Attributes

- FraudCaseId
- ClaimId
- FraudScore
- InvestigationStatus

### Relationships

- Fraud Case belongs to Claim

---

## AI Assessment

Represents AI-generated recommendations.

### Attributes

- AssessmentId
- ClaimId
- Recommendation
- ConfidenceScore
- GeneratedAt

### Relationships

- Assessment belongs to Claim

---

## ROI Metric

Represents business value generated.

### Attributes

- MetricId
- MetricType
- Value
- GeneratedDate

### Examples

- HoursSaved
- CostSavings
- FraudAvoidance
- AIAdoption

---

# Domain Relationships

Customer
→ Policy

Policy
→ Claim

Claim
→ Document

Claim
→ AI Assessment

Claim
→ Fraud Case

AI Assessment
→ Executive Metrics

Fraud Case
→ Executive Metrics

---