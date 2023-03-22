pipeline {
  agent any
  stages {
    stage('docker build') {
      steps {
        sh 'sudo docker build https://github.com/swatiAga/project7-sourcecode.git#test:docker'
      }
    }

  }
}