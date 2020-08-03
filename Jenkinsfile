pipeline {
 agent any
 stages {
  stage('Stage One') {
   steps {
    echo 'Hi, it’s JavaStart'
   }
  }
  stage('Stage Two') {
   steps {
    input('Do you want to proceed?')
   }
  }
  stage('Stage  Three') {
   when {
    not {
     branch "master"
    }
   }
   steps {
    echo "Let’s start"
   }
  }
  stage('Stage Four') {
    parallel {
     stage('Stage Unit Test') {
      steps {
       echo "Running the unit test..."
      }
     }
     stage('Integration test') {
      steps {
       echo "Running the integration test..."
      }
     }
    }
  }
 }
} 