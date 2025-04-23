pipeline {
  agent any

  stages {
    stage('Clone Repo') {
      steps {
        git branch: 'main',
            credentialsId: 'github-token',
            url: 'https://github.com/manikantas123/food-donation-platform.git'
      }
    }

    stage('Build Docker Images') {
      steps {
        bat 'docker-compose build'
      }
    }

    stage('Run App') {
      steps {
        bat 'docker-compose up -d'
      }
    }
  }
}
