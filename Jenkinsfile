pipeline {
  agent any
  environment {
      DISABLE_AUTH = 'true'
      DB_ENGINE    = 'sqlite'
  }
 tools {maven "Maven-360"
        org.jenkinsci.plugins.docker.commons.tools.DockerTool "docker"
        }
   stages {
    stage('Build') {
      steps {
        //sh 'mvn clean package'
         sh "echo $DISABLE_AUTH "
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
