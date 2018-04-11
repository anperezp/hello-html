pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        docker {
          image 'ubuntu:latest'
          args '-p 80:80 '
        }
        
      }
      steps {
        echo 'La mona lisa esta despierta'
      }
    }
  }
}