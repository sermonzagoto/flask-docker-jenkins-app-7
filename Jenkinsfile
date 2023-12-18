pipeline {
    environment {
        dockerImage = ''
        registry = "sermon99/flask-docker-jenkins-app-7"
    }
    
    agent any

    stages {
        stage('Cloning the code') {
            steps {
                git branch: 'main', url: 'https://github.com/sermonzagoto/flask-docker-jenkins-app-7.git'
            }
        }
        stage('Build the image') {
            steps {
                git 'git@github.com:sermonzagoto/flask-docker-jenkins-app-7.git'
                sh 'docker build -t flask-docker-jenkins-app-7:v.7 .'
            }
        }
    }
}
