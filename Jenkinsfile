pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'master', url: 'https://github.com/teregudi/docker-react.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}
