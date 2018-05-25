pipeline {
  agent {
    docker {
      image 'ubuntu'
      args '-p 80:80'
    }
    
  }
  stages {
    stage('Apache') {
      steps {
        sh 'apt-get update && apt-get install -y apache2'
        sh 'service apache2 start'
      }
    }
    stage('Git') {
      steps {
        sh 'apt-get -y install git && rm -Rf hello-html'
        sh 'git clone https://github.com/anperezp/hello-html.git'
        sh 'cp index.html /var/www/index.html'
      }
    }
  }
}