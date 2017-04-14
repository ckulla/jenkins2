pipeline {
  agent none
  stages {
    stage('uberjar') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
    stage('java-test') {
      steps {
        sh 'echo "test1"'
      }
    }
  }
  triggers {
    pollSCM('* * * * *')
  }
}