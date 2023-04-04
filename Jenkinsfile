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

    stage('Deploying Istio scripts') {
      steps {
        script {
          kubernetesDeploy(configs: "release/*istio-manifests.yaml", kubeconfigId: "kubernetes")
        }

      }
    }

  }
}