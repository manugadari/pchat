pipeline {
  agent any

    stages {
    stage('checkout') {
      steps {
        git 'https://github.com/manugadari/pchat'
        sh 'git branch'
      }
    }
    stage('SAST Scan for whole project') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'UNSTABLE') {
                    sh "python3 snyk.py --scan-for-push"
                }
            }
        }
    stage('Build') {
      steps {
        sh 'python3 snyk.py --repo-path "https://github.com/manugadari/pchat.git" --base-branch "master" --pr-branch "feature-1" --scan-for-pr'                                 
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
