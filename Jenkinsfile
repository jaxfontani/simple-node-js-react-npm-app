pipeline {
  agent {
    docker {
      image 'node:lts-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      environment {
        HOME = '.'
      }
      steps {
        sh 'npm install'
      }
    }

    stage('List files') {
      parallel {
        stage('List files') {
          steps {
            sh 'ls -lR'
          }
        }

        stage('PWD') {
          steps {
            sh 'pwd'
          }
        }

      }
    }

  }
}