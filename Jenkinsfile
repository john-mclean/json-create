pipeline {
  agent any
  stages {
    stage('FirstStage') {
      steps {
        import groovy.json.*

        env = build.getEnvironment(listener)
        buildNumber = env.get('BUILD_NUMBER')
        commitHash = env.get('GIT_COMMIT')
        buildDate = System.currentTimeMillis()

        buildJson = JsonBuilder(build_number: buildNumber, commit_hash: commitHash, build_date: buildDate)
        json = buildJson.toPrettyString()

        println json

        new File(build.workspace.toString() + "\\build.json").write(json)
      }
    }
  }
}
