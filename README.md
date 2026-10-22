# BAYORA
## Securing Adversarial AI Safety Testing Infrastructure

**Team:** The Coders

**Tagline:** Test the attack. Prove the defense. Trust the result.

BAYORA is a prototype for secure adversarial AI safety testing. It
demonstrates a controlled evaluation workflow, simulated policy
outcomes, and hash-linked audit verification.

## Problem

Red-Team testing, Blue-Team defenses, and the model under evaluation
must operate without exposing sensitive information or invalidating
safety findings.

## Proposed Solution

BAYORA separates the evaluation workflow into controlled components:

- Red-Team test submission
- Control and policy layer
- Evaluation broker
- Model-under-test zone
- Blue-Team policy review
- Evidence and audit
- Observability and review dashboard

## Current Prototype Features

- FastAPI backend
- Interactive browser dashboard
- Request validation
- Simulated evaluation outcomes
- In-memory hash-linked audit events
- Audit verification endpoint
- Automated API tests
- Threat model and residual-risk documentation

## Technology Stack

- Python
- FastAPI
- HTML, CSS, JavaScript
- Pytest
- SHA-256 hashing

## Run Locally

Install dependencies:

    python -m pip install -r requirements.txt

Start the backend:

    python -m uvicorn backend.app:app --reload

Open `frontend/index.html` in a browser.

API documentation:

    http://127.0.0.1:8000/docs

Run tests:

    python -m pytest -q

See [docs/setup.md](docs/setup.md) for full instructions.

## Documentation

- [System Architecture](docs/architecture.md)
- [Threat Model](docs/threat-model.md)
- [Residual Risks](docs/residual-risk.md)
- [Setup Guide](docs/setup.md)
- [Demo Instructions](demo/demo-script.md)

## Current Limitations

This is a simulated prototype. It does not connect to a real LLM or
implement production-grade multi-tenant container isolation.

Audit events are stored in memory and are cleared when the backend
restarts. Passing tests validate the implemented prototype behaviour;
they do not prove complete security.

## Team

The Coders:
- Ananya Bansal
- Sparsh Dheer
- Akshay Singhal

## Responsible Use

Use BAYORA for authorized AI safety evaluation and defensive research.
