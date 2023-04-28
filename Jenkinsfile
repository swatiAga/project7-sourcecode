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
        sh '''pwd docker login -u mohdkhalid -p dckr_pat_K1C6BUyQ5rwcOxmHtiYAOa_wryo

syft packages mohdkhalid/adservice:86511cf  -o json  > adservice.json
syft packages mohdkhalid/currencyservice:86511cf  -o json  > currencyservice.json
syft packages mohdkhalid/shippingservice:86511cf  -o json  > shippingservice.json
syft packages mohdkhalid/frontend:86511cf  -o json  > frontend.json
syft packages mohdkhalid/paymentservice:86511cf  -o json  > paymentservice.json
syft packages mohdkhalid/cartservice:86511cf  -o json  > cartservice.json
syft packages mohdkhalid/recommendationservice:86511cf  -o json  > recommendationservice.json
syft packages mohdkhalid/productcatalogservice:86511cf  -o json  > productcatalogservice.json
syft packages mohdkhalid/emailservice:86511cf -o json  > emailservice.json
syft packages mohdkhalid/checkoutservice:86511cf  -o json  > checkoutservice.json
syft packages mohdkhalid/loadgenerator:86511cf  -o json  > loadgenerator.json

syft packages dir:./ --scope all-layers -o json  > sbom-msdemo.json

'''
      }
    }

  }
}
