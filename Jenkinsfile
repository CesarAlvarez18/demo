pipeline {
  agent any
  tools {
    nodejs 'node-11.1.0'
  }

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

   stages {
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
                    sh 'npm config ls'
                }
            }
        }
    stage('Run tests') {
      steps {
        sh 'cd jenkins-tests && npm t'
      }
    }
  }
}