# Decision Records

Key architectural and operational decisions, extracted from provided decision records and transcripts.

- Chose markdown over JSON for AI output due to token efficiency (ADR-007)
- Deferred async worker queue until >100 docs/min (ADR-012)
- Enforced zero content-loss guarantee via post-conversion validation (ADR-019)

## Open risks / warnings
- Large PDFs can cause memory spikes during conversion, potentially leading to outages (Incident 05-18)
