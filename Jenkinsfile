pipeline {
  agent any
 tools {maven "Maven-360"}
   stages {
    stage('Build') {
      steps {
         sh 'mvn clean package'
      }
    }
    stage('Docker') {
      steps {
        sh 'Docker '
      }
    }
  }
}
