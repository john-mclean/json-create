pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        echo 'not today'
      }
    }
  }
  post {
    always {
      ehco 'stuff'
    }
  }
}