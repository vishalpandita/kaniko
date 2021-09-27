pipeline {
  agent any
  stages {
    stage('build') {
      agent any
      steps {
        sh 'export IMAGE_ID=vishalpandita/sita '
        sh '''
 export IMAGE_TAG=$(git rev-parse HEAD)'''
        sh ' export DOCKER_CONFIG=/kaniko/.docker'
        sh '''docker build -t $IMAGE_ID:$IMAGE_TAG
.'''
        sh 'docker push'
      }
    }

  }
}