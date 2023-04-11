pipeline {
  agent any
  stages {
    stage('Quality Gate') {
      steps {
        sh '''sh \'\'\'sudo export PATH="$PATH:/opt/sonar-scanner/bin"

sudo sonar-scanner \\
  -Dsonar.projectKey=Project7 \\
  -Dsonar.sources=. \\
  -Dsonar.host.url=http://65.1.127.93:9000 \\
  -Dsonar.token=sqp_f216299d80f29d093feaa1f7b14014ed24231cfa\'\'\''''
      }
    }

  }
}