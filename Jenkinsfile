pipeline {
    agent {
        docker {
            image 'node:lts-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'sudo npm cache clean --force"
                sh 'npm install' 
            }
        }
    }
}
