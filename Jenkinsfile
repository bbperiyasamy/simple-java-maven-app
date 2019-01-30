pipeline {
  agent any
  environment {
      DISABLE_AUTH = 'true'
      DB_ENGINE    = 'sqlite'
  }
 tools {maven "Maven-360"}
   stages {
    stage('Build') {
      steps {
         sh 'mvn clean package'
         sh "echo $DISABLE_AUTH "
      }
    }
    stage('Docker') {
      steps {
        sh 'Docker '
      }
    }
  }
}
