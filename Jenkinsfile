pipeline {
  agent any
  stages {
    stage('Sonarqube') {
      steps {
        sh '''export PATH="$PATH:/opt/sonar-scanner/bin"
env | grep PATH
sonar-scanner -v
sonar-scanner \\
  -Dsonar.projectKey=test \\
  -Dsonar.sources=.  \\
  -Dsonar.host.url=http://3.110.192.225:9000 \\
  -Dsonar.exclusions=src/adservice/src/main/java/hipstershop/*  \\
  -Dsonar.login=sqp_b9e3a94438cf301b7b78ffe6a2b3c727befea627'''
      }
    }

  }
}