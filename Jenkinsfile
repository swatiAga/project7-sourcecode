pipeline {
  agent any
  stages {
    stage('List pods') {
      withKubeConfig([credentialsId: 'kubernetes-config']) {
          sh 'curl -LO "https://storage.googleapis.com/kubernetes-release/release/v1.20.5/bin/linux/amd64/kubectl"'  
          sh 'chmod u+x ./kubectl'  
          sh './kubectl get pods'
      }
    }
  stage('Deploying App to Kubernetes') {
      steps {
        script {
          sh 'kubectl apply -f release/*kubernetes-manifest.yml'
        }
      }
    }
  }
}
