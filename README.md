cat > README.md <<'README_EOF'
---
title: LLM Analysis Quiz Solver
emoji: 🏃
colorFrom: red
colorTo: blue
sdk: docker
sdk_version: "0.0.1"
app_file: main.py
pinned: false
app_port: 7860
---

# LLM Analysis Quiz Solver

**Author:** Naman Dhingra (GitHub: naman-dhingra)  
**Contact:** naman.dhingra@example.com

This repository is configured to run as a **Docker-based Hugging Face Space** (or locally using Docker).  
The FastAPI app entrypoint is **`main.py`** and the app listens on port **7860** by default.  
(Original README used as base: see project README). :contentReference[oaicite:2]{index=2}

---

## Quick overview

- `sdk: docker` indicates this Space expects a `Dockerfile` and will run inside a container.
- This README explains how to run locally with Docker and how to deploy to Hugging Face Spaces (Docker mode).
- The project exposes routes including `/healthz` and `/solve`. Example demo routes referenced in the original repo: `/demo` and `/demo2` — test after deployment.

---

## Prerequisites

- Docker installed locally (Docker Desktop or equivalent).
- (Optional) A Hugging Face account and `huggingface_hub` CLI token if you want to push to Spaces.
- Python 3.12+ for local development (project `pyproject.toml` targets 3.12). :contentReference[oaicite:3]{index=3}

---

## Local: build and run with Docker

Build the image (run in repo root where your `Dockerfile` is located):

```bash
docker build -t llm-analysis-quiz-solver:latest .
