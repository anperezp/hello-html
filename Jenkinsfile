pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        docker {
          image 'ubuntu'
          args '-p 80:80'
        }
        
      }
      steps {
        sh 'apt-get update'
        sh 'apt-get install -y apache2'
        sh 'apt-get -y install git'
        sh 'git clone https://github.com/anperezp/hello-html.git'
      }
    }
    stage('El Grito') {
      steps {
        echo 'No se que hago'
      }
    }
  }
}