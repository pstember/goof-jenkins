pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:12.7.0-alpine'
    }

  }
  stages {
    stage('Node') {
      steps {
        sh 'npm install'
      }
    }
    stage('Snyk') {
      steps {
        snykSecurity(failOnIssues: true, snykInstallation: 'Snyk')
      }
    }
  }
}