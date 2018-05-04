pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        dockerfile {
          filename '/home/ana/Docker/Dockerfile'
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