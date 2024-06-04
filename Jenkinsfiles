pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        
snykSecurity failOnError: false, organisation: 'PYTHON-APP', projectName: 'Python-game', severity: 'medium', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'        
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
