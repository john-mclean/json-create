pipeline {
  agent any
  stages {
    stage('BuildAndTest') {
      steps {
        echo 'build and test and stuff'
      }
    }
    stage('CreateBuildJson') {
      steps {
        sh '''BUILD_DATE=$(date +%s)
echo -e "{\\"build_number\\":"${BUILD_NUMBER}", \\"commit_hash\\":\\""$GIT_COMMIT"\\", \\"build_date\\":"$BUILD_DATE"}" > build.json
'''
      }
    }
  }
}