pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh 'echo \'hello\''
      }
    }

    stage('Syft SBOM') {
      
      steps {
        sh '''pwd docker login -u mohdkhalid -p dckr_pat__3TtkkQMmJfRLfZzdakx9x_jZEI

syft packages mohdkhalid/adservice:04a0f4c  -o json  > adservice.json
syft packages mohdkhalid/currencyservice:04a0f4c  -o json  > currencyservice.json
syft packages mohdkhalid/shippingservice:04a0f4c  -o json  > shippingservice.json
syft packages mohdkhalid/frontend:04a0f4c  -o json  > frontend.json
syft packages mohdkhalid/paymentservice:04a0f4c  -o json  > paymentservice.json
syft packages mohdkhalid/cartservice:04a0f4c  -o json  > cartservice.json
syft packages mohdkhalid/recommendationservice:04a0f4c  -o json  > recommendationservice.json
syft packages mohdkhalid/productcatalogservice:04a0f4c  -o json  > productcatalogservice.json
syft packages mohdkhalid/emailservice:04a0f4c -o json  > emailservice.json
syft packages mohdkhalid/checkoutservice:04a0f4c  -o json  > checkoutservice.json
syft packages mohdkhalid/loadgenerator:04a0f4c  -o json  > loadgenerator.json

syft packages dir:./ --scope all-layers -o json  > sbom-msdemo.json

'''
      }
    }

  }
}
