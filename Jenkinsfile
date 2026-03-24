
pipeline {
  agent any
  triggers { pollSCM('* * * * *') }

  stages {
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
    stage 'test' {
    steps {
    echo "Building test for ${platform}"
    }
    }
    }
    }
    }
    }
}
}
