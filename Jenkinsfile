pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        build 'Build'
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