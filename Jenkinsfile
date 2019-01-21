pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        build 'Build 1'
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