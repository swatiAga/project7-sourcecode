pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh 'echo \'hello\''
      }
    }

    stage('Skaffold Build') {
      agent {
        node {
          label 'DeploymentServer'
        }

      }
      steps {
        sh '''pwd docker login -u agarwalswati -p dckr_pat__3TtkkQMmJfRLfZzdakx9x_jZEI

skaffold build --default-repo docker.io/agarwalswati
'''
      }
    }

  }
}
