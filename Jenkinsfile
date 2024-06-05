pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
        sh'git diff [<feature-1] -- [<main>]'
      }
    }
  }
}
