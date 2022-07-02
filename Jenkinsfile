pipeline {
  agent any

  stages {

    stage('TEST1') {
      steps {
        echo 'Test1'
      }
    }

    stage('TEST2') {
      steps {
        echo 'Test2'
      }
    }

  }

  post {
    fixed {
      echo "Hello"
    }
    failed {
      echo "Failed State"
    }
    cleanup {
      echo "Common steps"
    }
  }

}
