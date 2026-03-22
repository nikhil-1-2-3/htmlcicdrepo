pipeline {
  agent any

  stages {

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t singhnikhil212/stream-ui .'
      }
    }

    stage('Push to Docker Hub') {
      steps {
        sh 'docker push singhnikhil212/stream-ui'
      }
    }

  }
}
