pipeline {
  agent any
  stages {
  stage('Sanity check') {
      steps {
        input "Does the staging environment look ok?"
      }
  }    
    stage('Stage 1') {
      steps {
        echo 'kdfkdjfkj'
      }
    }
  }
  post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
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
