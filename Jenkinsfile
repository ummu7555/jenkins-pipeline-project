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
                echo "Build stage running (no docker used)"
            }
        }

        stage('Test') {
            steps {
                echo "Test stage running"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage completed (demo pipeline)"
            }
        }
    }
}
