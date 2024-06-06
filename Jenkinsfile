pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
        git branch: 'feature-1', url: 'https://github.com/manugadari/pchat'
        sh'git checkout feature-1'
        sh'git diff --name-only feature-1 main '
      }
    } 
    stage('Authorize Snyk CLI') {
            steps {
                withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
                    sh 'snyk auth ${SNYK_TOKEN}'
                }
             }
          }

        stage('SAST SCAN for modified files') {
            steps {
                sh 'snyk code test changes.py'
                }
            }
    
        stage('SAST SCAN for all files') {
            steps {
                sh 'snyk code test '
                }
          }
     }
}
