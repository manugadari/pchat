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
    stage('SAST scan for changed files') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'UNSTABLE') {
                  sh 'python3 snyk.py --repo-path "./" --base-branch "master" --pr-branch "feature-2" --scan-for-pr'  
                }
            }
      }
    // stage('SCA scan') {
    //     steps {
    //       sh "python3 snyk.py " +
    //           "--scan-for-pr"
    //   }
    // }
  }
}
