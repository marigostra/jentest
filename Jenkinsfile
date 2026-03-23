
pipeline {
  agent any
  triggers { pollSCM('* * * * *') }

  stages {
    stage('Checkout') {
      steps {
        sh 'git log'
      }
    }
}
}
