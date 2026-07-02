https://ummu7555.github.io/jenkins-pipeline-project/# 

🚀 CI/CD Pipeline Automation Using Jenkins

Automated CI/CD pipeline that builds, tests, and deploys a static Nginx-based website using Jenkins, Docker, and GitHub webhook integration — eliminating manual server login for every release.

![Jenkins](<img width="1920" height="1080" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/4e7ba82f-7435-4e35-abe5-0d983f964845" />
)
![Docker]<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/ddfe0781-a047-4230-b4ba-eadc55b388bb" />
)
---

## 📌 Overview

This project demonstrates a complete CI/CD workflow — every code push to GitHub automatically triggers a Jenkins pipeline that builds a Docker image, runs a basic health check, and deploys the containerized Nginx site. Built as part of hands-on DevOps practice to understand real-world automation, from source control to deployment.

## 🏗️ Architecture / Pipeline Flow

```
GitHub Push
     │
     ▼
GitHub Webhook Trigger
     │
     ▼
┌─────────────┐   ┌───────┐   ┌──────┐   ┌────────┐
│  Checkout   │──▶│ Build │──▶│ Test │──▶│ Deploy │
└─────────────┘   └───────┘   └──────┘   └────────┘
```

| Stage | What Happens |
|-------|---------------|
| **Checkout** | Jenkins pulls the latest code from GitHub via webhook trigger |
| **Build** | Docker image is built using the Dockerfile (Nginx + `index.html`) |
| **Test** | Basic health check confirms the container is serving content correctly |
| **Deploy** | Container is deployed and made accessible |

## 🛠️ Tech Stack

- **CI/CD:** Jenkins (Declarative Pipeline)
- **Containerization:** Docker
- **Web Server:** Nginx
- **Version Control:** Git & GitHub (Webhooks)
- **Cloud:** AWS EC2

## 📂 Project Structure

```
jenkins-pipeline-project/
├── Dockerfile      # Defines the Nginx container image
├── Jenkinsfile     # 4-stage declarative pipeline definition
└── index.html      # Static website content
```

## ⚙️ How It Works

1. Developer pushes code to the `main` branch on GitHub.
2. A GitHub webhook automatically triggers the Jenkins pipeline.
3. Jenkins checks out the latest code.
4. A Docker image is built from the `Dockerfile`.
5. A health check verifies the container is running and serving traffic.
6. The container is deployed — no manual server login required.

## 📸 Pipeline in Action

> .<img width="1598" height="306" alt="WhatsApp Image 2026-07-03 at 3 45 41 AM" src="https://github.com/user-attachments/assets/1594dc58-1290-4305-b92d-3434f303587c" />


```
![Jenkins Pipeline Success](screenshots/pipeline-success.png)
```

## 🚀 Run Locally

```bash
# Clone the repository
git clone https://github.com/ummu7555/jenkins-pipeline-project.git
cd jenkins-pipeline-project

# Build the Docker image
docker build -t jenkins-pipeline-demo .

# Run the container
docker run -d -p 80:80 jenkins-pipeline-demo
```

Visit `http://localhost` to view the deployed site.

## 💡 Key Learnings

- Setting up a Declarative Jenkins pipeline from scratch
- Integrating GitHub webhooks for automated build triggers
- Writing and optimizing a Dockerfile for a lightweight Nginx deployment
- Automating repetitive deployment steps to reduce manual effort

## 👩‍💻 Author

**Saniya Ayaz Shaikh**
📍 Pune, Maharashtra | [GitHub](https://github.com/ummu7555) | saniyaashaikh2244@gmail.com

---

