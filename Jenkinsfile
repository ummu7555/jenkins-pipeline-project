pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo "Cloning repository..."
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Building Docker image..."
                sh 'docker build -t jenkins-pipeline-project .'
            }
        }

        stage('Stop Old Container (if running)') {
            steps {
                echo "Stopping old container..."
                sh 'docker stop jenkins-container || true'
                sh 'docker rm jenkins-container || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo "Running new container..."
                sh 'docker run -d -p 8002:80 --name jenkins-container jenkins-pipeline-project'
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully 🚀"
        }
        failure {
            echo "Pipeline failed ❌ check logs"
        }
    }
}
