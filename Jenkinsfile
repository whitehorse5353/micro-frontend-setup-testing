pipeline {
  agent {
    node {
      label 'node_pre_build'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/whitehorse5353/micro-frontend-setup-testing', branch: 'master', changelog: true)
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