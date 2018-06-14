pipeline {
  agent any
  stages {
    stage('build') {
      steps {
	writeFile file: "application.sh", text: "echo Built ${BUILD_ID} of ${JOB_NAME}"
	archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'build successful'
      }
    }
    stage('test') {
      steps {
        echo 'test successful'
      }
    }
    stage('deploy') {
      steps {
        echo 'deploy successful'
      }
    }
  }
}
