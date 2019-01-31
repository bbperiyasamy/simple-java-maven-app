#!groovy
def awsRegion = "us-east-1"

pipeline {
  agent any
  environment {
      DISABLE_AUTH = 'true'
      DB_ENGINE    = 'sqlite'
  }
 tools {maven "Maven-360"  }
   stages {
    stage('Build') {
      steps {
        //sh 'mvn clean package'
         sh "echo $DISABLE_AUTH "
         sh "echo ${awsRegion}"
         sh "echo "Running ${env.BUILD_ID}on${env.JENKINS_URL}"
      }
    }
    stage('Docker') {
        steps {
    //  script {
    //  def  dockerfile = 'Dockerfile.test'
    //   }
        sh 'echo Docker '
      }
    }
  }
}
