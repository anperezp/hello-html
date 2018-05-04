pipeline {
  agent none
  stages {
    stage('MonaLisa') {
      parallel {
        stage('MonaLisa') {
          agent {
            docker {
              args '-p 80:80 '
              image 'ubuntu'
            }
            
          }
          steps {
            echo 'La mona lisa esta despierta'
            sh 'apt-get update'
            sh 'apt-get install -y apache2'
          }
        }
        stage('El Grito') {
          agent {
            dockerfile {
              filename 'DockerFile'
            }
            
          }
          steps {
            echo 'Prueba Dockerfile'
            sh '''#Imagen base
FROM ubuntu
'''
          }
        }
      }
    }
  }
}