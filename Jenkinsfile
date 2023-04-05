pipeline {
  agent any
  stages {
      stage('Deploying App to Kubernetes') {
      steps {
        script {
          sh 'kubectl apply -f release/*kubernetes-manifest.yml'
        }
      }
    }
  }
}
