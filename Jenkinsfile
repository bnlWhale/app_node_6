pipeline {
  agent {
    docker {
      image 'image \'node:6-alpine\''
      args 'args \'-p 3000:3000\''
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }
  }
}