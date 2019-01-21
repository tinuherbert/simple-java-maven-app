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
        bat 'mvn deploy:deploy-file -DrepositoryId=organisation-internal -Durl=http://localhost:8081/artifactory/NousDevops -DgroupId=test -DartifactId=test -Dversion=1.1 -Dpackaging=jar -Dfile=target/test-1.1.jar'
      }
    }
  }
}