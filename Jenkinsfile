pipeline {
  agent any
  stages {
      stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "kubernetes-manifests.yml", kubeconfigId: "kubernetes")
        }
      }
    }

  }
}
