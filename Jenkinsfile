pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm install --save-dev cross-env'

            }
        }
        stage('Deliver') {
                    steps {
                        docker version
                        input message: 'Finished using the web site? (Click "Proceed" to continue)'
                    }
                }
        
    }
}
