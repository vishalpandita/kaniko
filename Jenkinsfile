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
        sh 'cat /kaniko/.docker/config.json'
      }
    }

  }
}