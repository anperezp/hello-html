pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        docker {
          args '-p 80:80 '
          image 'ubuntu'
        }
        
      }
      steps {
        echo 'La mona lisa esta despierta'
        sh 'sudo apt-get update'
        sh 'sudo apt-get install -y apache2'
      }
    }
  }
}