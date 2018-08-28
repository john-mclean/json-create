pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        sh '''BUILD_DATE=$(date +%s)
echo "$BUILD_DATE"
echo -e "{\\"build_number\\":"${BUILD_NUMBER}" }"
echo -e "{\\"commit_hash\\":\\""$GIT_COMMIT"\\" }"
echo -e "{\\"build_date\\":"$BUILD_DATE" }"
'''
      }
    }
  }
}