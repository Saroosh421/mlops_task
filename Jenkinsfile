pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'docker build -t temp:latest .'
      }
    }
    stage('Deploy') {
      steps {
        bat 'docker run -d -p 8000:5000 temp'
      }
    }
  }
}