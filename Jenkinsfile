pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o YOUR_SRN-1 YOUR_SRN-1.cpp'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './YOUR_SRN-1'
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
