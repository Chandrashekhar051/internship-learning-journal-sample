# Week 2 – Session 3  
## Codespaces, Hugging Face Spaces & GitHub Actions

### Overview

In this session, I explored cloud-based development using GitHub Codespaces, deployed a FastAPI app using Hugging Face Spaces with Docker, and automated tasks using GitHub Actions. The focus was on moving from local development to cloud-native workflows.

---

## 1. GitHub Codespaces

GitHub Codespaces provides a full VS Code environment in the cloud directly connected to a repository.

Key learnings:

- No need to install dependencies locally.
- Environment is defined using `.devcontainer/devcontainer.json`.
- Extensions and tools can be pre-configured.
- `postCreateCommand` installs required packages automatically.

This removes system configuration issues and ensures the same setup for everyone working on the project.

---

## 2. Deploying with Hugging Face Spaces

A FastAPI application was deployed using Hugging Face Spaces with Docker.

Steps followed:

- Created a new Space.
- Selected Docker as runtime.
- Cloned the Space repository.
- Added `app.py`, `requirements.txt`, and `Dockerfile`.

The Dockerfile:

- Used Python base image.
- Installed dependencies.
- Ran the app with `uvicorn` on port `7860`.

After pushing the code, Hugging Face automatically built the container and deployed the app.

An access token was generated for authentication while pushing. It must be stored securely and never hardcoded.

---

## 3. GitHub Actions Automation

GitHub Actions was used to automate workflows inside the repository.

- Workflows are written in YAML inside `.github/workflows/`.
- Jobs run on GitHub-hosted runners.
- Steps can execute scripts, install dependencies, or push updates.

In the example shown:

- Python was set up.
- Data was fetched using a script.
- Changes were committed automatically by GitHub Actions.

This demonstrated basic CI/CD automation in practice.

---

## Key Takeaways

- Codespaces enables cloud-based development.
- Devcontainers ensure consistent environments.
- Docker simplifies deployment.
- Hugging Face Spaces supports container-based apps.
- GitHub Actions automates repetitive tasks.
- Secrets and tokens must be handled securely.

This session connected development, deployment, and automation into a practical cloud workflow.
