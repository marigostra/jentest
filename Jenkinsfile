
pipeline {
  agent any
  triggers { pollSCM('* * * * *') }

  stages {
    stage('Checkout') {
      steps {
        sh 'git log'
      }
    }

post {
always {
sh 'echo always'
}
}
}
}
