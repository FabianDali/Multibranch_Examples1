pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Build') {
      steps {
        echo ‘ Working with multibranch pipelines’
      }
    }
    stage (‘Proving’) {
	Steps {
		Echo ‘ Proving changes in my Jenkinsfile’
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
































































 






