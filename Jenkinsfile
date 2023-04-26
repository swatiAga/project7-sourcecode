pipeline {
  agent any
  stages {
    stage('Static Analysis') {
      steps {
        sh '''export PATH=$PATH:/opt/sonar-scanner/bin

        sonar-scanner \\
          -Dsonar.projectKey=Project7_TestBranch_26April2023 \\
          -Dsonar.sources=. \\
          -Dsonar.exclusions=src/adservice/src/main/java/hipstershop/** \\
          -Dsonar.host.url=http://3.110.116.139:9000 \\
          -Dsonar.login=sqp_52474af01718f5163b024e736d97b15c767b99c3'''
      }
    }

  }
}