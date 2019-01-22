pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        bat 'mvn clean package'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            bat 'mvn test'
            echo 'Tested'
          }
        }
        stage('Verify') {
          steps {
            bat 'mvn verify'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        bat 'mvn deploy -DaltDeploymentRepository=central::default::http://localhost:8081/artifactory/NousDevops'
      }
    }
  }
}