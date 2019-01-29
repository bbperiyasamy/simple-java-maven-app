pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo Build stage'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'echo test stage '
            }
        }
        stage('deployment') {
            steps {
                  sh 'echo deploy  stage  '
            }
        }
    }
}
