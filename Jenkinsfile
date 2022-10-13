pipeline {
  agent any

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

   stages {
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 11.1.0', configId: '<config-file-provider-id>') {
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