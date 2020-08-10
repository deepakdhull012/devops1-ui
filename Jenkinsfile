pipeline {
    agent any
    stages {
        stage('npm install') {
            steps {
                bat 'npm install'
            }
        }
        stage('build') {
            steps {
                bat 'npm run ng build --prod'
            }
        }
        stage('test') {
            steps {
                bat 'npm run ng test'
            }
        }
        stage('docker build') {
            steps {
                bat 'docker build ./ -t devops'
            }
        }
        stage('docker remove container') {
            steps {
                
                bat 'docker stop devops || true && docker rm devops || true'
            }
        }
        stage('docker deployment') {
            steps {
                bat 'docker run --detach --publish 80:80 --name devops devops'
            }
            
        }
        stage('final') {
            steps {
                bat 'echo ${BUILD_NUMBER}'
            }
            
        }
    }
}