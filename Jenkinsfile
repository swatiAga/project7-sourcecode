pipeline {
  agent any
  stages {
    stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "release/*.yml", kubeconfigId: "kubernetes")
        }

      }
    }
  }
}
