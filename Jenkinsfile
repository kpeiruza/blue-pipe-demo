pipeline {
  agent {
    label 'centos'
  }
  stages {
    stage('Build') {
      post {
        success {
          sh 'echo Funciona'
        }

      }
      steps {
        git 'https://github.com/kpeiruza/blue-pipe-demo/'
        container(name: 'centos') {
          sh 'yum --version'
          sh ''' echo 1
                echo 2
                echo 3
                '''
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo Soy un test'
      }
    }

  }
}