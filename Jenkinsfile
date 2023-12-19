pipeline {
    environment {
        dockerImage = ''
        registry = "sermon99/flask-docker-jenkins-app-7"
    }
    
    agent any

    stages {
        stage('Build the image') {
            steps {
                dockerImage = docker.build registry + ":$BUILD_NUMBER"
            }
        }
    }
}
