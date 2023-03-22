pipeline {
  agent any
  stages {
    stage('dockerbuild') {
      steps {
        withGradle() {
          sh 'docker build'
        }

      }
    }

  }
}