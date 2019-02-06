#!groovy
def awsRegion = "us-east-1"
//Peri added for testing added
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
         sh "echo Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
       }
    }
    stage('Docker') {
        input {
            message "Should we continue?"
            ok "Yes, we should."
            submitter "alice,bob"
            parameters {
                string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            }
        }
        steps {
    //  script {
    //  def  dockerfile = 'Dockerfile.test'
    //   }
        sh 'echo Docker '
        sh  "echo Hello, ${PERSON}, nice to meet you."
      }
    }
  }
}
