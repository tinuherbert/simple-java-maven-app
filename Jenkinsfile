pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        bat 'mvn package'
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
        bat './jenkins/scripts/deliver.sh'
      }
    }
  }
}