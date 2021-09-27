pipeline {
  agent any
  stages {
    stage('build') {
      agent any
      steps {
        sh 'IMAGE_ID=vishalpandita/sita '
        sh '''
 IMAGE_TAG=$(git rev-parse HEAD)'''
        sh ' export DOCKER_CONFIG=/kaniko/.docker'
        sh '''docker build -t $IMAGE_ID:$IMAGE_TAG 
.'''
        sh 'docker push'
      }
    }

  }
}