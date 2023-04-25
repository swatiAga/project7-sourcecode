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

    stage('Static Analysis') {
      steps {
        sh '''export PATH=$PATH:/opt/sonar-scanner/bin

        sonar-scanner \\
          -Dsonar.projectKey=Project7 \\
          -Dsonar.sources=. \\
          -Dsonar.host.url=http://13.235.255.168:9000 \\
          -Dsonar.token=sqp_f216299d80f29d093feaa1f7b14014ed24231cfa'''
      }
    }

  }
}