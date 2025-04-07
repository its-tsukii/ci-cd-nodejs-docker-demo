# 🚀 Node.js App CI/CD with Docker & GitHub Actions

[![Build and Push Docker Image](https://github.com/its-tsukii/ci-cd-nodejs-docker-demo/actions/workflows/main.yml/badge.svg)](https://github.com/its-tsukii/ci-cd-nodejs-docker-demo/actions/workflows/main.yml)

This project demonstrates a simple yet powerful DevOps pipeline that:

- Dockerizes a Node.js application
- Builds the Docker image using GitHub Actions
- Pushes the image to Docker Hub automatically on every `push` to the `main` branch

---

## 📦 Docker Image

👉 [blackplayer1001/node-app on Docker Hub](https://hub.docker.com/r/blackplayer1001/node-app)

---

## 🛠️ Tech Stack

- Node.js
- Docker
- GitHub Actions (CI/CD)
- Docker Hub

---

## 📁 Project Structure

. ├── .github 
    │ └── workflows 
    │ └── docker-publish.yml # CI/CD Workflow file 
    ├── Dockerfile # Docker build config 
    ├── index.js # Main application file 
    ├── package.json 
    └── README.md



---

## ⚙️ How It Works

1. On every push to the `main` branch:
   - GitHub Actions triggers a workflow
   - Builds the Docker image using your `Dockerfile`
   - Logs into Docker Hub using secrets (`DOCKER_USERNAME`, `DOCKER_PASSWORD`)
   - Pushes the image to your Docker Hub repository

2. Done! Your Docker image is live and ready to deploy anywhere.

---

## 🚀 Getting Started Locally

```bash
# Clone the repo
git clone https://github.com/its-tsukii/ci-cd-nodejs-docker-demo.git
cd ci-cd-nodejs-docker-demo

# Build the Docker image
docker build -t node-app .

# Run the container
docker run -p 3000:3000 node-app

# Open in browser
http://localhost:3000

🔐 GitHub Secrets Required
Make sure to add the following secrets in your GitHub repo:

Secret Name	Value
DOCKER_USERNAME	your Docker Hub username
DOCKER_PASSWORD	your Docker Hub password/token

🙌 Credits
Original code: heroku/node-js-sample

CI/CD and Docker pipeline by @its-tsukii
