pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build(job: 'Build', quietPeriod: 10)
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