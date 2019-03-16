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
                        docker run  -i -t  6-alpine /bin/bash


                        input message: 'Finished using the web site? (Click "Proceed" to continue)'
                    }
                }
        
    }
}
