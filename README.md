# 🚀 Automated CI/CD Pipeline using Jenkins, Docker & AWS

## 📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline for deploying a Dockerized web application on AWS EC2 using Jenkins and GitHub Webhooks.

Whenever code is pushed to GitHub, Jenkins automatically:

- Clones the latest code
- Builds a Docker image
- Stops the existing container
- Deploys the latest version
- Makes the updated website available instantly

---

## 🛠️ Tech Stack

- AWS EC2
- Ubuntu Linux
- Git
- GitHub
- Jenkins
- Docker
- Nginx
- GitHub Webhooks

---

## 📂 Project Architecture

![Architecture](screenshots/architecture.png)

---

## 🔄 CI/CD Workflow

```
Developer
     │
 git push
     │
     ▼
 GitHub Repository
     │
 GitHub Webhook
     ▼
 Jenkins Pipeline
     │
 Checkout Code
     │
 Build Docker Image
     │
 Stop Old Container
     │
 Run New Container
     ▼
 AWS EC2
```

---

## ⚙️ Jenkins Pipeline Stages

- Checkout Source Code
- Validate Project Files
- Build Docker Image
- Stop Existing Container
- Remove Old Container
- Deploy New Container

---

## 📷 Screenshots

### Website

![Website](screenshots/website.png)

---

### Jenkins Pipeline

![Pipeline](screenshots/pipeline-success.png)

---

### GitHub Webhook

![Webhook](screenshots/github-webhook.png)

---

### Docker Images

![Docker](screenshots/docker-images.png)

---

## 🚀 Deployment Steps

```bash
git clone git@github.com:YOUR_USERNAME/company-website.git

cd company-website

docker build -t company-website .

docker run -d \
--name website-container \
-p 80:80 \
company-website
```

---

## 📚 Learning Outcomes

- Linux Administration
- Git & GitHub
- Docker Image Creation
- Docker Container Deployment
- Jenkins Pipeline
- GitHub Webhooks
- CI/CD Automation
- AWS EC2 Deployment

---

## 👨‍💻 Author

Ram Kumar

GitHub: https://github.com/NemesisPrimee
