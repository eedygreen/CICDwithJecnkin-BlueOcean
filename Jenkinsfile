pipeline {
  agent {
    docker {
      image 'node:6-alpine'
    }

  }
  stages {
    stage('Build') {
      agent {
        docker {
          image 'node:6-alpine'
          args '-p 3000:3000'
        }

      }
      environment {
        cli = 'true'
      }
      steps {
        sh 'npm install'
      }
    }

  }
  environment {
    cli = 'true'
  }
}