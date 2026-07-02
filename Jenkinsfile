pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/ummu7555/jenkins-pipeline-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop jenkins-app-container || true'
                sh 'docker rm jenkins-app-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name jenkins-app-container jenkins-app'
            }
        }
    }
}

