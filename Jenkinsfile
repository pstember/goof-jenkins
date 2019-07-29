pipeline {
  agent {
    docker {
      image '12.7.0-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Node') {
      steps {
        sh 'npm install'
      }
    }
  }
}