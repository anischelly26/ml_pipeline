<div align="center">

# ML PIPELINE

### End-to-end machine learning workflow · distributed training services · deployment architecture

[![Python](https://img.shields.io/badge/Python-ML-111111?style=for-the-badge&logo=python)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Orchestration-111111?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Supabase](https://img.shields.io/badge/Supabase-Data-111111?style=for-the-badge&logo=supabase)](https://supabase.com/)
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-ML%20Services-111111?style=for-the-badge)](https://huggingface.co/)

**[LIVE FRONTEND ↗](https://ml-pipeline-roan.vercel.app)**

</div>

---

## Overview

This repository contains an **end-to-end ML pipeline architecture** that separates the machine-learning lifecycle into deployable services:

```text
DATASET
  ↓
01 // INGEST + PROFILE
  ↓
02 // CLEAN + FEATURE ENGINEERING
  ↓
03 // TRAIN + EVALUATE
  ↓
04 // EXPLAIN + REPORT
  ↓
RESULTS / STATUS / PERSISTENCE
```

A FastAPI backend orchestrates the pipeline, the individual ML stages can run as Hugging Face Spaces, run metadata can be persisted in Supabase, and the frontend can be deployed independently on Vercel.

## Architecture

```text
Browser / Frontend
       ↓
   FastAPI API
       ↓
┌───────────────────────────────┐
│  Space 1 · Ingest + Profile   │
│  Space 2 · Clean + Engineer   │
│  Space 3 · Train + Evaluate   │
│  Space 4 · Explain + Report   │
└───────────────────────────────┘
       ↓
 Supabase / Run State
```

## Repository map

```text
ml_pipeline/
├── backend/          # FastAPI orchestration service
├── database/         # Supabase / PostgreSQL migration
├── frontend/         # browser UI + Vercel configuration
├── spaces/           # four independently deployable ML stages
├── .github/          # repository automation
└── DEPLOYMENT_GUIDE.md
```

## Deployment model

The project is designed around independently deployable components:

- **Hugging Face Spaces** → ML execution stages
- **FastAPI / Render** → orchestration API
- **Supabase** → database and pipeline state
- **Vercel** → frontend hosting

See [`DEPLOYMENT_GUIDE.md`](./DEPLOYMENT_GUIDE.md) for the complete deployment flow.

---

## Provenance / collaboration

This repository is a **fork of [`adam12bT/ml_pipeline`](https://github.com/adam12bT/ml_pipeline)** by **Adam Bouacida**.

I keep this fork in my engineering portfolio as a **collaborative / learning codebase**, not as a solo-authored project. The upstream repository and its original work remain credited to Adam. Any changes or extensions made specifically in this fork can be tracked through its commit history.

---

## Portfolio context

I am interested in systems that connect **machine learning with real software architecture**: data ingestion, APIs, distributed model services, persistence, deployment and user-facing products.

This repository complements my work across computer vision, explainable AI, recommendation systems and full-stack engineering.

<div align="center">

**ANIS CHELLI** · Software Engineering · AI × Product Engineering

[GitHub Profile](https://github.com/anischelly26)

</div>
