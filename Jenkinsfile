pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/pranav9989/docker-prac.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                dir('DockerJenkinsExperiment') {  // Ensure Docker build happens in the right folder
                    bat 'ls -l'  // Debugging: List files to check if Dockerfile exists
                    bat 'docker build -t my-docker-webapp .'  // Build Docker Image
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:80 my-docker-webapp'
            }
        }
    }
}
