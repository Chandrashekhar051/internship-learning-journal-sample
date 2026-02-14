# Week 2 – Session 2  
## Podman, GitHub Pages, FastAPI & Deployment

### Overview

In this session, I learned how containers work in real-world development, how to deploy static and backend applications, and how to expose local applications securely. The session connected DevOps concepts with practical deployment workflows.

---

## 1. Containers vs Virtual Machines

The session started by explaining the core difference between virtual machines and containers.

- Virtual Machines include a full guest operating system.
- Containers share the host OS kernel.
- Containers are lightweight and start much faster.
- Containers are ideal for microservices and modern development workflows.

This clarified why containerization is preferred for scalable applications.

---

## 2. Podman vs Docker

I learned that:

- Both Podman and Docker are container engines.
- Podman is daemonless (no background service required).
- Podman supports rootless containers.
- Docker relies on a central daemon.
- Commands are mostly compatible between the two.

Podman provides better security architecture due to rootless execution.

---

## 3. GitHub Pages – Static Site Deployment

GitHub Pages allows hosting static websites directly from a repository.

Key points learned:

- It works only for static content (HTML, CSS, JS).
- It can be enabled from repository settings.
- Deployment happens automatically from a selected branch.
- No backend support (only frontend hosting).

This helped understand the difference between static and dynamic deployments.

---

## 4. FastAPI – Building APIs

FastAPI was introduced as a modern Python framework for building APIs.

I understood:

- FastAPI is based on ASGI.
- It automatically generates interactive API documentation.
- It supports GET and POST methods.
- It uses Pydantic for request validation.

FastAPI is lightweight, fast, and ideal for building backend services.

---

## 5. HTTP Methods – GET vs POST

The session explained:

- GET → Used to retrieve data.
- POST → Used to send data to the server.
- Data in GET appears in the URL.
- POST sends data in the request body.

This clarified how APIs communicate with clients.

---

## 6. FastAPI Interactive Docs

FastAPI automatically generates:

- `/docs` (Swagger UI)
- `/redoc`

These help test endpoints without external tools.

This simplifies backend testing during development.

---

## 7. Vercel Deployment

Vercel was introduced as a cloud platform for deployment.

I learned:

- Vercel is great for frontend and serverless functions.
- It can deploy directly from GitHub.
- It also supports CLI-based deployment.
- Free tier has execution time limits.

Important limitation:
Long-running backend processes may timeout in Vercel’s free tier.

---

## 8. Deploying with Vercel CLI

The deployment flow included:

- Installing Vercel CLI
- Logging in
- Running deployment commands
- Linking project to GitHub

This demonstrated real-world CI/CD workflow.

---

## 9. Local Development with ngrok

ngrok was introduced to expose local servers to the internet.

I learned:

- It creates a secure public URL for local apps.
- Useful for testing webhooks and remote access.
- Temporary URLs are generated.
- Helpful during backend development and testing.

---

## 10. Managing Secrets & Environment Variables

The session emphasized security:

- Never hardcode API keys.
- Use environment variables.
- Store secrets securely in deployment platforms.
- Use `.env` files locally.

This reinforced secure development practices.

---

## 11. Understanding CORS

CORS (Cross-Origin Resource Sharing) was explained as:

- A browser security feature.
- Prevents unauthorized cross-domain requests.
- Needs proper configuration in backend.
- Required when frontend and backend run on different domains.

This clarified why APIs sometimes fail due to CORS errors.

---

## Key Takeaways

- Containers are lightweight alternatives to VMs.
- Podman offers daemonless and rootless containerization.
- GitHub Pages is suitable for static websites.
- FastAPI simplifies backend API development.
- Vercel supports quick deployment but has time limits.
- ngrok helps expose local servers.
- Proper secret management is essential.
- CORS must be configured correctly in distributed applications.

---

This session connected containerization, backend development, and deployment into a practical workflow that mirrors real-world development environments.
