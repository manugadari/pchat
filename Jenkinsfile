pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
        sh'git diff master feature-1'
      }
    }
  }
}
