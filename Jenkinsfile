pipeline {
  agent any

  stages {

    stage('Build Docker Image') {
      steps {
        bat 'docker build -t singhnikhil212/stream-ui .'
      }
    }

    stage('Push to Docker Hub') {
      steps {
        bat 'docker push singhnikhil212/stream-ui'
      }
    }

  }
}
