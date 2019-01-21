pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        bat 'sh mvn -B -DskipTests clean package'
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