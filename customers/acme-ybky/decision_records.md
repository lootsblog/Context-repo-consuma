# Decision Records

Key architectural and operational decisions extracted from provided decision records and transcripts.

- ADR-003: gRPC between services for typed contracts and low latency
- ADR-009: cart state externalized to Redis so cartservice stays stateless and horizontally scalable
- ADR-014: each service owns its Dockerfile; deploys are gated through Skaffold + Kustomize per environment
