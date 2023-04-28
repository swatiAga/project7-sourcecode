pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh 'echo \'hello\''
      }
    }

    stage('Skaffold Build') {
      
      steps {
        sh '''pwd docker login -u agarwalswati -p dckr_pat__3TtkkQMmJfRLfZzdakx9x_jZEI

syft packages agarwalswati/adservice:6d829bf  -o json  > adservice.json
syft packages agarwalswati/currencyservice:6d829bf  -o json  > currencyservice.json
syft packages agarwalswati/shippingservice:6d829bf  -o json  > shippingservice.json
syft packages agarwalswati/frontend:6d829bf  -o json  > frontend.json
syft packages agarwalswati/paymentservice:6d829bf  -o json  > paymentservice.json
syft packages agarwalswati/cartservice:6d829bf  -o json  > cartservice.json
syft packages agarwalswati/recommendationservice:6d829bf  -o json  > recommendationservice.json
syft packages agarwalswati/productcatalogservice:6d829bf  -o json  > productcatalogservice.json
syft packages agarwalswati/emailservice:6d829bf -o json  > emailservice.json
syft packages agarwalswati/checkoutservice:6d829bf  -o json  > checkoutservice.json
syft packages agarwalswati/loadgenerator:6d829bf  -o json  > loadgenerator.json

syft packages dir:./ --scope all-layers -o json  > sbom-msdemo.json

'''
      }
    }

  }
}
