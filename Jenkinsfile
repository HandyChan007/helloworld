pipeline {
  agent any
  stages {
    stage('Sanity check') {
      steps {
        input 'Does the staging environment look ok?'
      }
    }
    stage('Stage 1') {
      parallel {
        stage('Stage 1') {
          steps {
            echo 'kdfkdjfkj'
          }
        }
        stage('s1') {
          steps {
            echo '123'
          }
        }
      }
    }
  }
  post {
    always {
      echo 'One way or another, I have finished'
      deleteDir()

    }

    success {
      echo 'I succeeeded!'

    }

    unstable {
      echo 'I am unstable :/'

    }

    failure {
      echo 'I failed :('

    }

    changed {
      echo 'Things were different before...'

    }

  }
}