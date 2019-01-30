node{
    def mvnHome = tool name: 'maven-360', type: 'maven'
    def mvn = "${mvnHome}/bin/mvn"
	stage('Git Checkout'){
	   git branch: 'master',
	       credentialsId: 'github',
		   url: 'https://github.com/javahometech/my-app'
	}

	stage('Build'){
	   sh "${mvn} clean package"
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
