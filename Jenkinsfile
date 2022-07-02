//pipeline {
//  agent any
//
//  stages {
//
//    stage('TEST1') {
//      steps {
//        echo 'Test1'
//      }
//    }
//
//    stage('TEST2') {
//      steps {
//        echo 'Test2'
//        emailext body: 'TEST', subject: 'TEST', to: 'raghu@local.com'
//        build job: 'roboshop-ansible', parameters: [string(name: 'COMPONENT', value: 'frontend')]
//      }
//    }
//
//  }
//
//  post {
//    fixed {
//      echo "Hello"
//    }
//    failure {
//      echo "Failed State"
//      emailext body: 'TEST', subject: 'TEST', to: 'raghu@local.com'
//    }
//    cleanup {
//      echo "Common steps"
//    }
//  }
//
//}


pipeline {
  agent any

  environment {
    SAMPLE_URL="google.com"
    SSH = credentials("SSH")
  }

  stages {

    stage("One") {
      steps {
        sh 'echo URL = ${SAMPLE_URL}'
        echo SAMPLE_URL
        echo SSH
      }
    }

  }
}

//env.SAMPLE_URL="google.com"
//node() {
//  stage("One - ${SAMPLE_URL}") {
//    echo SAMPLE_URL
//  }
//}
