pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'slave'
        }

      }
      steps {
        sh 'echo "Hello World"'
        sh 'ls -ltr'
        sh 'pwd'
        sh '''echo "it will make to next branch"
'''
      }
    }

  }
}