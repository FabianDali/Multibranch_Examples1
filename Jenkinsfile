pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Build') {
      steps {
        echo 'Working with multibranch pipelines'
      }
    }
    stage ('Proving') {
	    steps {
		     echo 'Proving changes in my Jenkinsfile'
      }
    }
    stage ('cat README') {
      when  {
            branch  "fix-*"
      }
      steps  {
          bat '''cat README.md '''
      }
    }
  }
  post {
    always {
        junit(
          allowEmptyResults: true, 
          testResults: '**/build/test-results/test/*.xml'
        )
    }
  }
}




























































































































































 






