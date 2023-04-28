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
        sh '''pwd docker login -u mohdkhalid -p dckr_pat_K1C6BUyQ5rwcOxmHtiYAOa_wryo

skaffold build --default-repo docker.io/mohdkhalid
'''
      }
    }

  }
}