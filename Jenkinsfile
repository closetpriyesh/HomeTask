pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'echo building'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'echo test'
          }
        }

        stage('API_Test') {
          steps {
            echo 'echo API Tests'
          }
        }

      }
    }

    stage('Notify') {
      steps {
        echo 'echo notify'
      }
    }

  }
}