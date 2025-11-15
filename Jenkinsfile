pipeline {
    agent any

    stages {
        stage('docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    ls -al
                    node --version
                    npm build
                    ls -al
                '''
            }
        }
    }
}
