pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh 'echo \'hello\''
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''export PATH=$PATH:/opt/sonar-scanner/bin

        sonar-scanner \\
          -Dsonar.projectKey=Project7April262023 \\
          -Dsonar.sources=. \\
          -Dsonar.exclusions=src/adservice/src/main/java/hipstershop/** \\
          -Dsonar.host.url=http://13.200.12.129:9000 \\
          -Dsonar.login=sqp_4e7b4a89ef8158f6744ee9c8676f8008dff0a762
          '''
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
skaffold build --default-repo docker.io/agarwalswati'''
      }
    }

  }
}