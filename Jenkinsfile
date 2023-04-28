pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh 'echo \'hello\''
      }
    }
stage('Skaffold Push') {
      agent {
        node {
          label 'DeploymentServer'
        }

      }
      steps {
        sh '''pwd docker login -u agarwalswati -p dckr_pat__3TtkkQMmJfRLfZzdakx9x_jZEI

skaffold push --default-repo docker.io/agarwalswati
'''
      }
    }

  }
}
