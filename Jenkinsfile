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


//pipeline {
//  agent any
//
//  environment {
//    SAMPLE_URL="google.com"
//    SSH = credentials("SSH")
//  }
//
//  parameters {
//    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//
//    text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//
//    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//
//    choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//
//    password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//  }
//
//  triggers { pollSCM('* * * * *') }
//
//  stages {
//
//    stage("One") {
//      steps {
//        sh 'echo URL = ${SAMPLE_URL}'
//        echo SAMPLE_URL
//        echo SSH
//        echo PERSON
//      }
//    }
//
//  }
//}

//env.SAMPLE_URL="google.com"
//node() {
//  stage("One - ${SAMPLE_URL}") {
//    echo SAMPLE_URL
//  }
//}
//

//pipeline {
//  agent any
//  tools {
//    maven 'maven'
//  }
//  stages {
//    stage('Maven Version') {
//      input {
//        message "Should we continue?"
//        ok "Yes, we should."
//        submitter "admin"
//        parameters {
//          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//        }
//      }
//      steps {
//        sh 'mvn --version'
//      }
//    }
//  }
//}


//pipeline {
//  agent any
//
//  stages {
//    stage('one') {
//      steps {
//        echo 'ONE'
//      }
//    }
//    stage('two') {
//      when {
//        expression {
//          BRANCH_NAME == "master"
//        }
//      }
//      steps {
//        echo 'TWO'
//      }
//    }
//  }
//
//
//}


pipeline {
  agent any
  stages {
    stage('S1') {
      steps {
        echo 'S1'
      }
    }
    stage('S2') {
      steps {
        echo 'S2'
      }
    }
    stage('Parallel Stages') {
      parallel {
        stage('P1') {
          steps {
            sh 'sleep 120'
          }
        }
        stage('P2') {
          steps {
            sh 'sleep 120'
          }
        }
        stage('P3') {
          steps {
            sh 'sleep 120'
          }
        }
      }
    }
  }
}


















