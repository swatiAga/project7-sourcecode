pipeline {
  agent any
  stages {
      stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "/var/lib/jenkins/workspace/testKubernetes_test/release/kubernetes-manifests.yml", kubeconfigId: "kubernetes")
        }
      }
    }

  }
}
