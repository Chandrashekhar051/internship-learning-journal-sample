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
