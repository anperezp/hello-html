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
        sh 'clone https://github.com/anperezp/hello-html.git'
      }
    }
  }
}