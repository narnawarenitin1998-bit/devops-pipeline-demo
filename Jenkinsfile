cat <<EOF > Jenkinsfile
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
                sh 'docker build -t demo-app:latest .'
            }
        }
        stage('3. Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s-manifest.yaml'
            }
        }
    }
}
EOF
