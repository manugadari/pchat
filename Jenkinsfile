pipeline {
  agent any

    stages {
    stage('Build') {
      steps {
        git 'https://github.com/manugadari/pchat'
      }
    }
    stage('Build') {
      steps {
        sh "python3 snyk.py " +
           "--repo-path https://github.com/manugadari/pchat"
      }
    }
  }
}
