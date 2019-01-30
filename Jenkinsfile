#!groovy
def mvnHome =  tool name: 'maven-360', type: 'maven'
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {

              sh "${mvnHome}/bin/mvn package"
              sh 'echo Build stage'
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
