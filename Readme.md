# Hello World Docker Image

This repository provides a guide to build, push, and run a simple Docker image. The image is hosted on Docker Hub under `mirotivo/hello-world`.

---

## 1. Build and Push to Docker Hub

To build the Docker image locally and push it to Docker Hub, use the following commands:

```bash
docker build -t mirotivo/hello-world:latest .
docker push mirotivo/hello-world:latest
```

## 2. Set Up Docker on a Linux Alpine Server

Follow these steps to install and configure Docker on your Linux Alpine server:

```bash
# Step 1: Update the Package Index
sudo apt-get update
# Step 2: Install Docker
sudo apt-get install -y docker.io
# Step 3: Add Current User to the Docker Group
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

## 3. Run the Docker Image

Run the Docker container on the server with the following command:

```bash
docker run -p 8080:80 "mirotivo/hello-world:latest"
```

## 4. Test the Server Locally

Verify that the server is running by using curl to send a request to the local server:

```bash
curl http://127.0.0.1:8080
```

