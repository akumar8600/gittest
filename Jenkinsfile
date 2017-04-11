pipeline {
  agent none
  stages {
    stage('DEV') {
      steps {
        echo 'hello world'
      }
    }
    stage('REG') {
      steps {
        sleep 5
      }
    }
    stage('STG') {
      steps {
        build 'Build_Package_TEST'
      }
    }
  }
}