pipeline {
  agent any
  stages {
    stage('use the sh file') {
      steps {
        sh '#sh \'/var/lib/jenkins/workspace/tShellScriptFileWithJenkins_test/hack/make-release.sh\''
      }
    }

    stage('test') {
      steps {
        sh '\'echo $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u agarwalswati --password-stdin\'  '
      }
    }

  }
}