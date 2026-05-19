
pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:sivaram2662/jenkinsapp-sample.git'
            }
        }
         stage('docker-version') {
            steps {
                sh 'docker --version'
            }
        }
        stage('docker-build') {
            steps {
                sh 'sudo docker build  -t apache:3 . '
                sh 'sudo docker images'
                sh 'sudo docker images -a'
            }
        }
        stage('docker-container') {
            steps {
                sh 'sudo docker run  -d -p 8085:80 apache:3'
                sh 'sudo docker ps '
                sh 'sudo docker ps -a'
            }
        }
         stage('ecr-image') {
            steps {
                sh 'aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 607856468790.dkr.ecr.us-east-1.amazonaws.com'
                sh 'sudo docker build -t 607856468790.dkr.ecr.us-east-1.amazonaws.com/ecrimages:latest .'
                sh 'sudo docker push 607856468790.dkr.ecr.us-east-1.amazonaws.com/ecrimages:latest'
            }
        }
    }
}

















