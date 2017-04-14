pipeline {
  //git poll: true, intervall: '* * * * *', url: 'git@github.com:ckulla/jenkins2.git'
  agent none
  stages {
    stage('uberjar') {
      agent any
      steps {
        sh 'echo "Hello World"'
      }
    }

    stage('java-test') {
      parallel 
          test1: {
              node('any') {
                  checkout scm
                  sh 'echo test1'
              }
          },
          test2: {
              node('any') {
                  checkout scm
                  sh 'echo test2'
              }
          }
       }
    }
}