pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        
        sh'git checkout origin feature-1'
        sh'git checkout feature-1'
        sh'git diff master feature-1'
      }
    }
  }
}
