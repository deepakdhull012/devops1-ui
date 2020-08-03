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
        // stage('test') {
        //     steps {
        //         bat 'npm run ng test'
        //     }
        // }
    }
}