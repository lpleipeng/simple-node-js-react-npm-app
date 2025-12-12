pipeline {
    agent any
    tools {
        nodejs 'NODE_HOME'  
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build Project') {
            steps {
                sh 'npm run build'
            }
        }
    }
}