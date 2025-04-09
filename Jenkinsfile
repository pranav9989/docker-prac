pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/pranav9989/myfirst.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "Building Docker image..."
            }
        }

        stage('Run Docker Container') {
            steps {
                echo "Running Docker container..."
            }
        }
    }
}
