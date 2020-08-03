pipeline {
    agent any
    stages {
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
    }
}