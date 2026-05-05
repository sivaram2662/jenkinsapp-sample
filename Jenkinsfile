
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
                sh 'sudo docker build  -t apache:1 . '
                sh 'sudo docker images'
                sh 'sudo docker images -a'
            }
        }
        stage('docker-container') {
            steps {
                sh 'sudo docker run  -d -p 8000:80 apache:1'
                sh 'sudo docker ps '
                sh 'sudo docker ps -a'
            }
        }
    }
}





