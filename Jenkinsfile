pipeline {
  agent none
  stages {
    stage('Checkout Code') {
      steps {
        svn(url: 'http://svn-azure.livecareer.com/svn/configurations/trunk/livecareer/trunk', poll: true)
      }
    }
  }
}