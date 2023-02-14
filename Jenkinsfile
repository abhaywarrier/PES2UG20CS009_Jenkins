pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES2UG20CS09 PES2UG20CS009.cpp'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES2UG20CS009'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
        echo 'Deployment successful'
      }
    }
  }
  
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
