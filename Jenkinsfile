
pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:sivaram2662/jenkinsapp-sample.git'
            }
        }
        //  stage('docker-images') {
        //     steps {
        //         sh 'docker build images -t apache:1 .'
        //     }
        // }
    }
}





