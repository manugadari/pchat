pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
        git branch: 'feature-1', url: 'https://github.com/manugadari/pchat'
        sh'git checkout feature-1'
        sh'sudo git diff master feature-1 >> /modified'
      }
    }
  }
}
