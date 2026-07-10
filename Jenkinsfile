pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t company-website:latest .'
            }
        }

        stage('Stop Old Container') {
            steps {
                echo 'Stopping old container if it exists...'
                sh 'docker stop website-container || true'
                sh 'docker rm website-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                echo 'Starting new container...'
                sh '''
                docker run -d \
                --name website-container \
                -p 80:80 \
                company-website:latest
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful!'
        }

        failure {
            echo 'Deployment Failed!'
        }
    }
}
