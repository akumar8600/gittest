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
            echo 'Final Deployment on Production completed Successfully.'
            
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