pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'docker'
        }

      }
      steps {
        sh 'export IMAGE_ID=vishalpandita/sita '
        sh '''
 export IMAGE_TAG=$(git rev-parse HEAD)'''
        sh ' export DOCKER_CONFIG=/kaniko/.docker'
        sh 'docker build -t vishalpandita/sita "."'
        sh 'docker push'
      }
    }

  }
}