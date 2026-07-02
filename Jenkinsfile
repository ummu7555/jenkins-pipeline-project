pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/ummu7555/jenkins-pipeline-project.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build running successfully"
            }
        }

        stage('Test') {
            steps {
                echo "Testt running successfully"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy completed successfully"
            }
        }
    }
}

