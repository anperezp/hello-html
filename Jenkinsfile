pipeline {
  agent {
    docker {
      image 'ubuntu'
      args '-p 80:80'
    }
    
  }
  stages {
    stage('Container') {
      agent {
        docker {
          image 'ubuntu'
          args '-p 80:80'
        }
        
      }
      steps {
        sh 'apt-get update'
      }
    }
    stage('Apache') {
      steps {
        sh 'apt-get install -y apache2'
        sh 'service apache2 start'
      }
    }
    stage('Git') {
      steps {
        sh 'apt-get -y install git'
        sh 'git clone https://github.com/anperezp/hello-html.git'
        sh 'cd /hello-html'
        sh 'cp index.html /var/www/index.html'
      }
    }
  }
}