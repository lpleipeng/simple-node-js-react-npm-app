pipeline {
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                    export PATH="/var/lib/jenkins/.nvm/versions/node/v24.12.0/bin:$PATH"
                    /var/lib/jenkins/.nvm/versions/node/v24.12.0/bin/npm install
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    export PATH="/var/lib/jenkins/.nvm/versions/node/v24.12.0/bin:$PATH"
                    /var/lib/jenkins/.nvm/versions/node/v24.12.0/bin/npm run build
                '''
            }
        }
    }
}
