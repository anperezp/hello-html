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
        git 'https://github.com/anperezp/hello-html'
        sh 'apt-get install -y git && git clone git://github.com/anperezp/hello-html'
        sh 'apt-get update'
        sh 'apt-get install -y apache2'
        sh 'cp hello-html/index.html /var/www/html/index.html'
        sh 'service apache2 restart'
      }
    }
  }
}