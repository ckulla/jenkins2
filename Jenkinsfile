pipeline {
  agent none
  stages {
    stage('uberjar') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
    stage('build') {
       agent any
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
    stage('regression test') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
    stage('promote') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }
  }
  triggers {
    pollSCM('* * * * *')
  }
}