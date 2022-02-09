pipeline {

  agent {
    label 'kube-slave'
  }
  
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/rbouikila/hellowhale.git', branch:'master'
      }
    }
        
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "hellowhale.yml")
        }
      }
    }

  }

}
