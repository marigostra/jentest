
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

def job = Jenkins.instance.getItemByFullName("luwrain/main")  
if (!job) {  
  println "Project not found: ${projectName}"  
  return  
}  

}

}
}
}
