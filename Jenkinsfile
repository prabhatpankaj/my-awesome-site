pipeline {
  agent { label 'docker' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  triggers {
    cron('@daily')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -f "Dockerfile-terraform" -t brightbox/terraform:latest .'
        sh 'docker build -f "Dockerfile-cli" -t brightbox/cli:latest .'
      }
    }
  }
}
