
pipeline {
  agent any
  triggers { pollSCM('* * * * *') }

  stages {
  stage ('Prepare') {
  steps {
  sh 'echo preparing stage'
  }
  }
    stage('Checkout') {
    matrix {
    agent any
    axes {
    axis {
    name 'platform'
    values 'linux', 'windows'
    }
    }
    
    stages {
    stage ('test') {
    steps {
    echo "Building test for ${platform}"
    }
    }
    }
    }
    }
    }

post {
always {
sh 'echo post 1'
}

success {
sh 'echo post 2'
}



}
}
