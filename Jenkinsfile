pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS078-1'
        sh 'g++ Jenkins_lab-main/main/hello.cpp -o output'
        echo 'Build Stage Successful'
      }
    }
    stage('Test') {
      steps {
        sh './output1'
        echo 'Test Stage Successful'
        }
      }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
