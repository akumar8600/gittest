pipeline {
  agent none
  stages {
    stage('DEV') {
      steps {
        parallel(
          "DEV": {
            echo 'hello world'
            
          },
          "Auto-Test": {
            sleep 10
            
          }
        )
      }
    }
    stage('REG') {
      steps {
        parallel(
          "REG": {
            sleep 5
            
          },
          "Auto-Reg": {
            echo 'test Automation'
            
          }
        )
      }
    }
    stage('STG') {
      steps {
        parallel(
          "STG": {
            build 'Build_Package_TEST'
            
          },
          "Auto-STG": {
            sleep 10
            
          }
        )
      }
    }
    stage('Prod') {
      steps {
        echo 'Deployed'
      }
    }
  }
}