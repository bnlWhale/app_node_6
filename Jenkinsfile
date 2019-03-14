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
            }
        }
        stage('Deliver') {
                    steps {
                        sh 'pwd'
                        docker run --rm -i -t alpine /bin/sh './jenkins/deliver.sh'
                        input message: 'Finished using the web site? (Click "Proceed" to continue)'
                    }
                }
        
    }
}
