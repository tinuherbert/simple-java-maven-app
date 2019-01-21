pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        bat(script: 'mvn package', returnStatus: true)
      }
    }
    stage('Test') {
      steps {
        bat 'mvn test'
        echo 'Tested'
      }
    }
    stage('Deploy') {
      steps {
        bat 'mvn deploy'
      }
    }
  }
}