# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] Returns JSON with fields: answer, confidence (0‑1), hallucination (bool)
- [ ] Confidence <0.6 when at least one factual claim is unsupported by the knowledge base
- [ ] Response latency ≤2 seconds for a 7B model on a consumer GPU
- [ ] Loads ≥10 k passages in ≤5 minutes
- [ ] Embeddings stored with metadata (title, url)
- [ ] Search returns top‑5 passages within 100 ms
- [ ] Agreement score correlates with confidence (higher agreement → higher confidence)
- [ ] Sampler can be toggled via request flag
- [ ] Set up repo, CI pipeline, Docker skeleton
- [ ] Create CLI to download & preprocess small Wikipedia dump (~10 k articles)
- [ ] Generate embeddings with sentence‑transformers and load into Postgres pgvector
- [ ] Unit tests for CLI loader, vector search, and scoring functions (pytest)
- [ ] Integration test: end‑to‑end POST /detect returns schema‑valid JSON
- [ ] Load test with locust: 50 concurrent users for 5 min
- [ ] Build multi‑stage Docker image
- [ ] Deploy with Docker Compose on a single‑GPU VM (e.g., AWS g4dn.xlarge)
- [ ] Expose API via Traefik with TLS termination
- [ ] Add OpenTelemetry collector to ship traces to Grafana Cloud

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
