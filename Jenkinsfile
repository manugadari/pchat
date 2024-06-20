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
        sh 'python3 snyk.py --repo-path "https://github.com/manugadari/pchat" --base-branch "master" --pr-branch "feature-1" --scan-for-push'
      }
    }
      stage('changed files') {
      steps {
        sh "python3 snyk.py " +
            "--scan-for-pr"
      }
    }
  }
}
