pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t jenkins-app .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker ps'
                sh 'docker run -d -p 8002:80 --name jenkins-app jenkins-app || true'
            }
        }
    }
}
