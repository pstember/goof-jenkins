pipeline {
  agent {
    docker {
      image '12.7.0-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Snyk') {
      steps {
        snykSecurity(failOnIssues: true, organisation: '9813a9b3-6a54-4c33-bff8-c1cb9c12b7fe', projectName: 'Jenking-goof', snykTokenId: 'bd8e4f88-15b2-434a-a528-54ef376e702d')
      }
    }
  }
}