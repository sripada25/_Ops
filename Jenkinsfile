pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
      }
      post {
        success {
          script {
            currentBuild.result = 'FAILURE'
          }
        }
      }
    }
  }
  post {
    always {
      echo currentBuild.currentResult
    }
  }
}