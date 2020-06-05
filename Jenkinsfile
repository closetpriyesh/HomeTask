pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing'
          }
        }

        stage('API_Test') {
          steps {
            echo 'API Testing'
          }
        }

      }
    }

    stage('Notify') {
      steps {
        echo 'Notifying'
      }
    }

  }
}