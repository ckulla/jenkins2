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
      agent any
      steps {
        parallel(
          "java-test1": {
            checkout scm
            sh 'cat Jenkinsfile'
            sh 'echo "test1"'
            
          },
          "java-test2": {
            checkout scm
            sh 'cat Jenkinsfile'
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