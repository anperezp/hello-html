pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      agent {
        dockerfile {
          filename 'Dockerfile'
        }
        
      }
      steps {
        echo 'La mona lisa esta despierta'
        sh 'apt-get update'
        sh 'apt-get install -y apache2'
        sh 'service apache2 start'
      }
    }
  }
}