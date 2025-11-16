pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Pulling latest code..."
                git branch: 'main', url: 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building Docker image..."
                sh 'docker build -t simple-app .'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo "No tests added, skipping..."'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying container..."
                sh 'docker run -d -p 5000:5000 --name simple-app simple-app || true'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
