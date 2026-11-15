pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t intellipaat-website:latest .'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                    docker rm -f intellipaat-website-container || true
                    docker run -d --name intellipaat-website-container -p 8084:80 intellipaat-website:latest
                '''
            }
        }
    }
}
