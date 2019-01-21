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
        bat(script: 'mvn test', returnStatus: true)
        echo 'Tested'
      }
    }
    stage('Deploy') {
      steps {
        bat(script: 'mvn deploy', returnStatus: true)
      }
    }
  }
}