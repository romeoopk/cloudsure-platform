# ADR-005: Adopt pgvector For Vector Search

## Status

Accepted

## Date

July 2026

---

# Context

CloudSure requires Retrieval Augmented Generation (RAG) capabilities.

The platform must store embeddings generated from:

- Policies
- Coverage Documents
- Claims Guidance
- Fraud Knowledge

---

# Decision

PostgreSQL with pgvector shall serve as the vector store.

---

# Rationale

Benefits:

- Existing PostgreSQL infrastructure
- Reduced complexity
- Open source
- Good Spring AI support

---

# Alternatives Considered

- Pinecone
- Weaviate
- Qdrant
- ChromaDB

---

# Consequences

Positive:

- Simplified architecture
- Reduced operational burden

Negative:

- Fewer advanced vector capabilities than dedicated platforms

---