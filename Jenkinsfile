pipeline {
  agent any
  stages {
    stage('Create Docker Image') {
      steps {
        sh './hack/make-release.sh'
      }
    }

  }
}