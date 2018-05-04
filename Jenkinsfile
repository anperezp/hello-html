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
        sh 'apt-get update'
        sh 'apt-get install -y apache2'
        sh 'service apache2 start'
        sh 'cp /home/ana/Docker/hello-html/index.html /var/www/html/index.html'
        sh 'service apache2 restart'
      }
    }
  }
}