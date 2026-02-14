## Containerization using Podman (Project 1 - Jupyter Lab)

### 1. Introduction to Containerization
In this session, I learned the fundamentals of containerization. Containers allow applications to run in isolated environments along with their dependencies. Unlike virtual machines, containers are lightweight and faster.

Podman is a container engine similar to Docker but daemonless and rootless by default.

---

### 2. Installing Podman in WSL

I installed Podman inside WSL (Ubuntu). During setup, additional packages like qemu-system-x86 were required.

Commands used:

sudo apt install qemu-system-x86
podman machine init
podman machine start

In WSL, permission issues with KVM were handled using:

sudo chmod 666 /dev/kvm

---

### 3. Pulling Container Images

I learned that container images are downloaded from container registries like Docker Hub or Quay.

Examples:

podman pull docker.io/library/nginx:latest
podman pull docker.io/library/alpine:latest

For Jupyter Lab:

podman pull quay.io/jupyter/base-notebook

To check downloaded images:

podman images

To remove an image:

podman rmi <image_id>

---

### 4. Running a Jupyter Notebook Container

After pulling the Jupyter base image, I created and ran a container.

Run container with port binding:

podman run -d --name jupyter_server -p 8888:8888 quay.io/jupyter/base-notebook

Check running containers:

podman ps

View logs:

podman logs jupyter_server

Stop and remove container:

podman stop jupyter_server
podman rm jupyter_server

---

### 5. Port Binding

Port binding allows accessing container services from the host machine.

Example:
-p 8888:8888

This maps:
Host Port 8888 → Container Port 8888

So Jupyter Lab becomes accessible at:
http://localhost:8888

---

### 6. Persisting Data using Volume Mounting

To avoid losing notebook data when the container stops, a directory was created and mounted.

mkdir jupyter_work
chmod 777 jupyter_work

Run with volume:

podman run -d -p 8888:8888 \
-v ~/jupyter_work:/home/jovyan/work \
--name jupyter_server \
quay.io/jupyter/base-notebook

This ensures notebook files are stored in the local system.

---

### Key Learnings

- Difference between Image and Container
- Pulling images from container registries
- Running containers with port binding
- Managing containers (start, stop, logs, remove)
- Persisting data using volume mounting
- Understanding container networking basics

Project 1 helped me understand how to containerize and run Jupyter Lab using Podman in WSL.

---

# Project 2: Containerizing Ollama for Local LLM

### 1. Running Ollama Container

Pulled and ran Ollama inside a Podman container.

Run Ollama container:

podman run -d docker.io/alpine/ollama

To enter inside container:

podman exec -it ollama sh

Inside container, verified ollama installation:

ollama

---

### 2. Running a Local LLM Model

Pulled and ran Gemma model inside container:

ollama run gemma3:270m

Verified model interaction inside container terminal.

---

# Project 3: Podman Networking (Inter-Container Communication)

### 1. Creating a Custom Network

To allow containers to communicate, created a bridge network:

podman network create ai

Check networks:

podman network ls

Remove network (if required):

podman network rm ai

---

### 2. Running Ollama on Custom Network

podman run -d \
--name ollama \
--network ai \
-p 11434:11434 \
docker.io/alpine/ollama

Port 11434 is used by Ollama API.

---

### 3. Running Jupyter on Same Network

podman run -d \
--name jupyter_server \
--network ai \
-p 8888:8888 \
-p 5000:5000 \
-v ~/jupyter_work:/home/jovyan/work \
quay.io/jupyter/base-notebook

Now both containers are connected via the same network (ai).

Important Concept:
Instead of using localhost, containers communicate using container name.

Example API URL inside Jupyter:

http://ollama:11434/api/chat

---

# API Calls Between Containers

Inside Jupyter Notebook:

import requests

def gemma3(user_prompt):
    url = "http://ollama:11434/api/chat"
    payload = {
        "model": "gemma:2b",
        "messages": [
            {
                "role": "system",
                "content": "You are a text summarizer/modifier."
            },
            {
                "role": "user",
                "content": user_prompt
            }
        ],
        "stream": False
    }

    response = requests.post(url, json=payload)
    return response.json()['message']['content']

This demonstrates inter-container API communication.

---

# Building a Flask Web App with LLM Backend

Ran a Flask-based application container:

podman run -d --name formalai -p 5000:5000 formalai

The Flask app:
- Sends request to Ollama API
- Receives LLM response
- Returns formatted output to browser

Architecture Learned:

User → Flask App → Ollama Container → Model Response → Flask → Browser

---

# Troubleshooting WSL Networking

Issues handled:
- Port binding conflicts
- Network creation/removal
- Container name resolution instead of localhost
- Ensuring containers run on same bridge network

---

# Key Learnings from Project 2 & 3

- Running Local LLM using Ollama inside container
- Pulling and executing Gemma model
- Understanding Podman bridge networking
- Inter-container communication using container names
- Making API calls between containers
- Integrating LLM with Flask backend
- Full-stack containerized architecture

This session helped me understand how multiple containers communicate and how to build an AI-powered web application using Podman.



