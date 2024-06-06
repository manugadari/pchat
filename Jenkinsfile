pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
        sh'git checkout origin feature-1'
        sh'git checkout feature-1'
        sh'git diff master feature-1'
      }
    }
  }
}
