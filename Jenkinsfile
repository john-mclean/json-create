pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        sh '''echo -e "{\\"build_number\\":"${BUILD_NUMBER}"}"
echo commit: $GIT_COMMIT
date +%s
'''
      }
    }
  }
}