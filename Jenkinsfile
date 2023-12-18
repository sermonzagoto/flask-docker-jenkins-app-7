pipeline {
    environment {
        dockerImage = ''
        registry = "sermon99/flask-docker-jenkins-app-7"
    }
    
    agent any

    stages {
        stage('Cloning the code') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'sermonzagoto', url: 'https://github.com/sermonzagoto/flask-docker-jenkins-app-7']])
            }
        }
        stage('Build image') {
            steps {
                sh 'docker build -t my-image:${BUILD_NUMBER} .'
            }
        }
    }
}
