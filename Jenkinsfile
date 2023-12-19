pipeline {
    environment {
        dockerImage = ''
        registry = "sermon99/flask-docker-jenkins-app-7"
    }
    
    agent any

    stages {
        stage('Clone the image') {
            steps {
                git 'https://github.com/sermonzagoto/flask-docker-jenkins-app-7.git'
            }
        }
        stage('Build the image') {
            steps {
                script {
                    dockerImage = docker.build registry + ":$BUILD_NUMBER"
                }
            }
        }
    }
}
