
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

post {
always {
echo "Getting log"
        script {
            def logContent = Jenkins.getInstance()
                .getItemByFullName(env.JOB_NAME)
                .getBuildByNumber(
                    Integer.parseInt(env.BUILD_NUMBER))
                .logFile.text
}

}
}
}
