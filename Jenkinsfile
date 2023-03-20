pipeline {
  agent any
  
  stages {
    stage('Installation') {
      steps {
        sh 'npm install'
      }
    }
    
    stage('Unit tests') {
      steps {
        sh 'npm run test'
      }
    }
    
    stage('E2E tests') {
      steps {
        sh 'npm run test:e2e'
      }
    }
    
    stage('Test coverage') {
      steps {
        sh 'npm run test:cov'
      }
    }
    
    stage('Build and deploy') {
      when {
        branch 'master'
      }
      steps {
        sh 'npm run build'
        // add commands to deploy the application
      }
    }
  }
}
