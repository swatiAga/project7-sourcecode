pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh 'sh $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u agarwalswati --password-stdin'
      }
    }

  }
}