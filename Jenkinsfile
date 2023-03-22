pipeline {
  agent any
  stages {
    stage('Sonarqube') {
      steps {
        sh '''export PATH="$PATH:/opt/sonar-scanner/bin"
env | grep PATH
sonar-scanner -v
sonar-scanner -X 
sonar-scanner \\
  -Dsonar.projectKey=test \\
  -Dsonar.sources=.  \\
  -Dsonar.host.url=http://3.108.225.19:9000 \\
  -Dsonar.qualitygate.wait=true \\
  -Dsonar.qualitygate.timeout=300 \\
  -Dsonar.exclusions=src/adservice/src/main/java/hipstershop/*  \\
  -Dsonar.login=sqp_b9e3a94438cf301b7b78ffe6a2b3c727befea627'''
      }
    }

  }
}