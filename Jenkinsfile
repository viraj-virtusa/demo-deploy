pipeline {

  agent { label 'master' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/viraj-virtusa/demo-deploy.git', branch:'test-deploy-stage'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "kubeconfig")
        }
      }
    }

  }

}
