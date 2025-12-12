pipeline {
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                sh '''
                    # 将 node 所在目录加入 PATH（关键！）
                    export PATH="/var/lib/jenkins/.nvm/versions/node/v24.12.0/bin:$PATH"
                    # 现在执行 npm 就能找到 node 了
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