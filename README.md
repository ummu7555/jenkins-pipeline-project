🔗 https://ummu7555.github.io/jenkins-pipeline-project/# 

🚀 CI/CD Pipeline Automation Using Jenkins
Automated CI/CD pipeline that builds, tests, and deploys a static Nginx-based website using Jenkins, Docker, GitHub, and GitHub Webhooks, eliminating manual deployment after every code change.
📌 Overview
This project demonstrates a complete CI/CD workflow. Every code push to GitHub automatically triggers a Jenkins pipeline that builds a Docker image, performs a basic health check, and deploys a containerized Nginx website. This project was built to gain hands-on experience with CI/CD automation using Jenkins.
🏗️ Architecture / Pipeline Flow
GitHub Push
     │
     ▼
GitHub Webhook Trigger
     │
     ▼
┌─────────────┐   ┌───────┐   ┌──────┐   ┌────────┐
│  Checkout   │──▶│ Build │──▶│ Test │──▶│ Deploy │
└─────────────┘   └───────┘   └──────┘   └────────┘
Stage
What Happens
Checkout
Jenkins pulls the latest code from GitHub
Build
Docker image is built using the Dockerfile
Test
Health check verifies the container is running correctly
Deploy
Docker container is started and the website is accessible
🛠️ Tech Stack
CI/CD: Jenkins (Declarative Pipeline)
Containerization: Docker
Web Server: Nginx
Version Control: Git & GitHub
Automation: GitHub Webhooks
📂 Project Structure
jenkins-pipeline-project/
├── Dockerfile
├── Jenkinsfile
├── index.html
└── README.md
⚙️ How It Works
Push code to the main branch on GitHub.
GitHub Webhook automatically triggers Jenkins.
Jenkins checks out the latest source code.
Jenkins builds a Docker image.
Jenkins performs a basic health check.
Jenkins deploys the Docker container automatically.
🚀 Run Locally
git clone https://github.com/ummu7555/jenkins-pipeline-project.git

cd jenkins-pipeline-project

docker build -t jenkins-pipeline-demo .

docker run -d -p 80:80 --name jenkins-container jenkins-pipeline-demo
Visit:
http://localhost
💡 Key Learnings
Built a Declarative Jenkins Pipeline
Configured GitHub Webhooks for automatic builds
Created a Dockerfile for an Nginx-based website
Automated build, test, and deployment using Jenkins
Reduced manual deployment effort through CI/CD automation
👩‍💻 Author
Saniya Ayaz Shaikh
📍 Pune, Maharashtra
GitHub: https://github.com/ummu7555⁠�


