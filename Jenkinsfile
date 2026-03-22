pipeline {
  agent any

  stages {

    stage('Build Docker Image') {
      steps {
        bat 'docker build -t singhnikhil212/stream-ui .'
      }
    }

    stage('Docker Login') {
      steps {
        withCredentials([usernamePassword(credentialsId: 'docker-creds', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
          bat 'docker login -u %DOCKER_USER% -p %DOCKER_PASS%'
        }
      }
    }

    stage('Push to Docker Hub') {
      steps {
        bat 'docker push singhnikhil212/stream-ui'
      }
    }

  }
}
