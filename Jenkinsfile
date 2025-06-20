pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/joaocjr97/atividade-modulo14.git'
            }
        }
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Start server') {
            steps {
                sh 'nohup npm start &'
                sh 'sleep 10'
            }
        }
        stage('Run Cypress tests') {
            steps {
                sh 'npx cypress run'
            }
        }
    }
}