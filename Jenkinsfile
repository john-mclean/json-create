pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        sh '''echo $BUILD_NUMBER
echo $GIT_COMMIT
date +%s
'''
      }
    }
  }
}