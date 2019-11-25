pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/whitehorse5353/micro-frontend-setup-testing', branch: 'release/*', changelog: true)
      }
    }

    stage('Install deps') {
      steps {
        sh 'npm install'
        sh 'npm test'
      }
    }

  }
}