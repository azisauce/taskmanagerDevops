pipeline {
  agent none
  stages {
    stage('Checking') {
      agent any
      steps {
        
        // sh 'docker build -t phpcomposer .'
        // sh 'docker images'
        sh 'docker version'
      }
    }
    stage('Build') {
      // agent { 
      //     docker {
      //       image 'phpcomposer'
      //     }
      // }
      agent any
      steps {
        
        // sh 'composer --version'
        // sh 'php --version'
        // sh 'composer install'
        // sh 'cp .env.example .env'
        // sh 'php artisan migrate --seed'
        // sh 'php artisan key:generate'
        sh 'cp .env.example .env'
        sh 'docker build -t mytaskmanagerproject-dockerized .'

      }
    }
    stage('Deploying') {
      agent any
      steps {
        
        // sh 'docker build -f Dockerfile-Laravel -t laravelproject .'
        // sh 'docker run -d -p 8881:80 laravelproject'
        sh ' Deploying...'
        sh 'docker images'

      }
    }
  }
}
