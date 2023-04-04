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
        sh 'kubectl apply -f release/*istio-manifests.yaml'
      }
    }

  }
}