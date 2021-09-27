pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'kaniko'
        }

      }
      steps {
        sh 'IMAGE_ID=vishalpandita/sita '
        sh '''
 IMAGE_TAG=$(git rev-parse HEAD)'''
        sh ' export DOCKER_CONFIG=/kaniko/.docker'
        sh '''kaniko/executor 
  --context $(pwd) 
  --dockerfile $(pwd)/Dockerfile 
  --destination $IMAGE_ID:$IMAGE_TAG 
  --destination $IMAGE_ID:latest 
  --force'''
      }
    }

  }
}