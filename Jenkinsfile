pipeline {
    agent any
    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/vand14vish2000-tech/ICONIC-APP.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Start Server') {
            steps {
                sh 'node server.js &'
            }
        }
    }
    post {
        success {
            echo '✅ Website Successfully Deployed!'
        }
        failure {
            echo '❌ Deployment Failed!'
        }
    }
}