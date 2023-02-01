pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/devopsdeepdive/blueocean-test-repo.git', branch: 'master', credentialsId: 'github-user')
      }
    }

    stage('Build') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

  }
}