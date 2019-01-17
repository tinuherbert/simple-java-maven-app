pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sleep 5
      }
    }
    stage('Test') {
      steps {
        echo 'Tested'
      }
    }
    stage('Deploy') {
      steps {
        mail(subject: 'Deploy', body: 'Deploy', to: 'tinuh@nousinfo.com')
      }
    }
  }
}