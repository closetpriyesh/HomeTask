pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Notify') {
      steps {
        echo 'Notifying'
      }
    }
    
    stage('archive') {
      steps {
        echo 'Archiving out!!'
        archiveArtifacts 'target/*.war'
      }
    }
    
    stage('Deploy') {
      steps {
        echo 'Deploying'
        deploy adapters: [tomcat9(credentialsId: 'MyTomcat', path: '', url: 'http://10.71.9.180:9999/')], contextPath: 'home', war: '**/*.war'
      }
    }
  }
}
