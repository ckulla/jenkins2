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
      parallel(
        "java-test1": {
          agent any
          steps {
              sh 'cat Jenkinsfile'
              sh 'echo "test1"'              
            }
          },
        "java-test2": {
          agent any
          steps {
              sh 'cat Jenkinsfile'
              sh 'echo "test2"'
            }
          }
       )
    }
  }
  triggers {
    pollSCM('* * * * *')
  }
}