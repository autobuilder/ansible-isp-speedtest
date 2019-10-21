pipeline {

  agent any

  stages {

    stage('Install kitchen environment') {
      steps {
        sh '''
        ansible --version
        vagrant --version
        chef gem install test-kitchen
        chef gem install kitchen-ansible
        chef gem install kitchen-vagrant
        '''
      }
    }

    stage('Linting using ansible-lint') {
      steps {
        sh 'ansible-lint .'
      }
    }

    stage('Provision kitchen environment') {
      steps {
        sh 'kitchen create'
      }
    }

    stage('Run ansible-role on environment') {
      steps {
        sh 'kitchen converge'
      }
    }

  }

}

