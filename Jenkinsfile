
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
                sh 'sudo docker build  -t apache:2 . '
                sh 'sudo docker images'
                sh 'sudo docker images -a'
            }
        }
        // stage('docker-container') {
        //     steps {
        //         sh 'sudo docker run  -d -p 8004:80 apache:1'
        //         sh 'sudo docker ps '
        //         sh 'sudo docker ps -a'
        //     }
        // }
        //  stage('ECR-Login') {
        //     steps {
        //         sh 'sudo aws ecr get-login-password --region ap-south-1 | sudo docker login --username AWS --password-stdin 607856468790.dkr.ecr.ap-south-1.amazonaws.com'
        //         sh 'sudo docker build -t jenkins-image:latest 607856468790.dkr.ecr.ap-south-1.amazonaws.com/jenkins-image:1.'
        //         sh 'sudo docker push 607856468790.dkr.ecr.ap-south-1.amazonaws.com/jenkins-image:1'
        //     }  
        // }
    }
}





