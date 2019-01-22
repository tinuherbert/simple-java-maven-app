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
        bat 'mvn deploy -DaltDeploymentRepository=central::default::http://localhost:8081/artifactory/NousDevops'
      }
    }
  }
}