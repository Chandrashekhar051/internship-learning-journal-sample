# Week 2 – Session 4  
## TDS Project Workflow & FastAPI Server Development

### Overview

In this session, I understood the complete TDS project workflow — from building a FastAPI backend to testing, containerizing, and deploying it. The focus was on writing structured APIs, validating data properly, handling file uploads, and preparing the project for deployment.

---

## 1. Understanding the Project Workflow

The session started with explaining how the TDS evaluation system works:

- Requests are sent in JSON format.
- The server processes and returns structured responses.
- Multiple rounds of evaluation may happen.
- Proper API structure is important for automation.

This clarified how backend APIs integrate with external systems.

---

## 2. FastAPI Setup & First GET Request

We created a basic FastAPI application:

- Installed FastAPI and Uvicorn.
- Created `app.py`.
- Defined a simple GET endpoint.
- Ran the server using:

```
uvicorn app:app --reload
```

This helped understand:
- FastAPI is ASGI-based.
- Uvicorn runs the application.
- GET requests are used to retrieve data.

---

## 3. Path & Query Parameters

I learned how to:

- Pass dynamic values in URL paths.
- Use query parameters for filtering.
- Handle parameters cleanly inside route functions.

This makes APIs more flexible and reusable.

---

## 4. Pydantic & Response Models

Pydantic was used for:

- Input validation.
- Data type enforcement.
- Structured response models.

Instead of manually checking inputs, Pydantic ensures:
- Correct data types.
- Required fields.
- Clean error handling.

This makes APIs production-ready.

---

## 5. POST Requests & Data Validation

POST endpoints were created to:

- Accept JSON request bodies.
- Validate input using Pydantic models.
- Return structured responses.

The difference between GET and POST became clearer:
- GET → Retrieve data
- POST → Send and process data

Validation ensures incorrect data does not break the application.

---

## 6. Uploading Files (Single & Multiple)

The session demonstrated:

- Uploading single files.
- Uploading multiple files.
- Handling file input in FastAPI.

This is useful for real-world APIs that accept documents or datasets.

---

## 7. Automated Testing with Curl & Copilot

APIs were tested using:

- `curl` commands from terminal.
- Postman.
- Copilot assistance for generating test commands.

This showed how APIs can be tested without frontend.

Automation improves reliability and saves time.

---

## 8. Secret Keys & Environment Variables

Sensitive values were stored in:

- `.env` file
- Environment variables

Important understanding:
- Never hardcode secret keys.
- Use environment-based configuration.
- Docker and deployment platforms support secret management.

This is critical for security.

---

## 9. Dockerfile Setup

A Dockerfile was created to containerize the FastAPI app.

Key components:

- Python base image.
- Working directory setup.
- Installing dependencies from `requirements.txt`.
- Running Uvicorn.
- Exposing the correct port.

This ensures the application runs consistently in any environment.

---

## 10. Deploying to Hugging Face

The containerized app was pushed to Hugging Face Spaces.

- Hugging Face built the Docker image.
- Installed dependencies.
- Started the FastAPI server.
- Generated a public URL.

This completed the full development-to-deployment cycle.

---

## 11. Bash Script for Live Testing

A bash script was created to:

- Automatically send test requests.
- Simulate evaluation calls.
- Reduce manual testing effort.

This makes the project more production-ready and testable.

---

## Key Takeaways

- FastAPI simplifies API development.
- Pydantic ensures strong validation.
- File uploads are easy to handle in FastAPI.
- Docker makes deployment consistent.
- Secrets must be managed securely.
- Automation improves reliability.
- Complete workflow: Build → Test → Containerize → Deploy.

This session helped connect backend development with real-world deployment and testing practices.
