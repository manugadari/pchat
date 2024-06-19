pipeline {
  agent any

    stages {
    stage('checkout') {
      steps {
        git 'https://github.com/manugadari/pchat'
      }
    }
    stage('Build') {
      steps {
        sh "python3 snyk.py " +
           "--scan-for-push"
      }
    }
  }
}
