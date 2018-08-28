pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        echo 'not today'
      }
    }
    stage('lastStage') {
      steps {
        sh '''BUILD_DATE=$(date +%s)
echo -e "{\\"build_number\\":"${BUILD_NUMBER}", \\"commit_hash\\":\\""$GIT_COMMIT"\\", \\"build_date\\":"$BUILD_DATE"}" > build.json
'''
      }
    }
  }
  post {
    always {
      echo 'stuff'

    }

  }
}