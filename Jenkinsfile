pipeline {
  agent {
    docker {
      image 'ubuntu'
      args '-p 80:80'
    }
    
  }
  stages {
    stage('Apache') {
      agent any
      steps {
        sh 'apt-get update && apt-get install -y apache2'
        sh 'service apache2 start'
      }
    }
    stage('Git') {
      steps {
        sh 'apt-get -y install git && rm -Rf hello-html'
        sh 'git clone https://github.com/anperezp/hello-html.git'
        fileExists 'index.html'
        dir(path: '/var/www')
        sh 'cp index.html index.html'
      }
    }
  }
}