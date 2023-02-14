pipeline {
  agent any
  tools { 
      maven 'Maven 3.9.0'
    }
  stages {
    stage('Bui1d') {
    steps {
      dir('/var/jenkins_home/workspace/PES2UG20CS009'){
      sh 'mvn clean install'
      echo 'Build stage successful '
      }
  }
}
stage('Test') {
  steps {
      dir('/var/jenkins_home/workspace/PES2UG20CS009'){
      sh 'mvn test'
      echo 'Test Stage Successful'
      post {
        always {
          junit 'target/surefire-reports/* .xml '
        }
      }
    }
  }
}
stage( 'Deploy') {
  steps {
    sh 'mvn deploy'
    echo 'Deployment Successful '
    }
  }
}
  
post {
  failure {
    echo 'pipeline failed'
    }
  }
}
