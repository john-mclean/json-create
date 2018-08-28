pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        sh '''echo -e "{\\"build_number\\":"${BUILD_NUMBER}" }"
'''
        sh '''echo -e "{\\"commit_hash\\":\\""$GIT_COMMIT"\\" }"
'''
        sh '''echo -e "{\\"build_date\\":"$(date +s%)" }"
'''
      }
    }
  }
}