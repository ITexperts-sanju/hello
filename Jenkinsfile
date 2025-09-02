pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ITexperts-sanju/hello.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t node-k8s-demo:1.0 .'
            }
        }
        stage('Deploy to Minikube') {
            steps {
                sh 'kubectl apply -f k8s-deployment.yaml'
            }
        }
    }
}
