pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'python3 snyk.py --scan-for-push'
            }
        }   
     } 
}
