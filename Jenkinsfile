pipeline {
  git poll: true, intervall: "* * * * * ", url: 'git@github.com:ckulla/jenkins2.git'
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
            sh 'echo test1'
            
          },
          "java-test2": {
            sh 'echo "test2"'
            
          },
          "ide": {
            sh 'echo "ide"'
            
          }

        )
      }
    }
  }
}