#!groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            def mvnHome =  tool name: 'maven-360', type: 'maven'
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
