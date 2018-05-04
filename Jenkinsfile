pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        docker {
          args '-p 80:80 '
          image 'ubuntu:latest'
        }
        
      }
      steps {
        echo 'La mona lisa esta despierta'
        sh 'apt-get update'
        sh 'apt-get install -y apache2'
      }
    }
  }
}