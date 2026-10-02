pipeline {
    agent any
    stages {
        stage('1. Checkout Code') {
            steps {
                echo 'Fetching code from Git...'
            }
        }
        stage('2. Build Docker Image') {
            steps {
                bat 'docker build -t demo-app:latest .'
            }
        }
        stage('3. Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s-manifest.yaml --validate=false'
            
            }
        }
    }
}
