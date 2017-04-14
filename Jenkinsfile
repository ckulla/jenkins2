pipeline {
  agent any
  stages {
    stage('uberjar') {
      steps {
        sh 'echo "Hello World"'
      }
    }
    stage('java-test1') {
      steps {
        parallel(
          "java-test1": {
            sh 'cat Jenkinsfile'
            
          },
          "java-test2": {
            sh 'echo "test2"'
            
          }
        )
      }
    }
    stage('java-test2') {
      steps {
        sh 'cat Jenkinsfile'
      }
    }
  }
}