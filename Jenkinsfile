pipeline {
  agent any
  stages {
      stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "/release/kubernetes-manifests.yml", kubeconfigId: "kubernetes")
        }
      }
    }

  }
}
