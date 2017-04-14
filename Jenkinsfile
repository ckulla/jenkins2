pipeline {
  agent none
  triggers { pollSCM('* * * * *') }
  stages {
    stage('uberjar') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
  }
}