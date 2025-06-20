pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                git branch: 'master', url: 'https://github.com/joaocjr97/atividade-modulo14.git'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'NO_COLOR=1 npm test'
            }
        }
        stage('Subir servidor') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
