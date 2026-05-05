
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
                sh 'docker build  -t apache:1 . '
                sh 'docker images'
                sh 'docker images -a'
            }
        }
    }
}





