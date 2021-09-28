pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'maven'
        }

      }
      steps {
        sh 'echo "Hello World"'
        sh 'ls -ltr'
        sh 'mvn'
        sh 'pwd'
      }
    }

  }
}