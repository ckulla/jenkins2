pipeline {
  agent none
  stages {
    stage('uberjar') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
    stage('java-test1') {
      steps {
        parallel(
          "java-test1": {
            sh 'echo "test1"'
            
          },
          "java-test2": {
            sh 'echo "test2"'
            
          }
        )
      }
    }
  }
  triggers {
    pollSCM('* * * * *')
  }
}