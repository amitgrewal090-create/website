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
                bat 'docker.exe build -t intellipaat-website:latest .'
            }
        }

        stage('Deploy Website') {
            steps {
                bat '''
                    docker.exe rm -f intellipaat-website-container 2>NUL
                    docker.exe run -d --name intellipaat-website-container -p 8084:80 intellipaat-website:latest
                '''
            }
        }
    }
}
