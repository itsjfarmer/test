pipeline {
  agent any
  stages {
    stage('build') {
      steps {
	properties([pipelineTriggers([[$class: 'GitHubPushTrigger'], pollSCM('* * * * *')])])
	writeFile file: "application.sh", text: "echo Built ${BUILD_ID} of ${JOB_NAME}"
	archiveArtifacts artifacts: '*.sh', fingerprint: true
        echo 'build successful'
	sleep 60
	//error("Build failed")
      }
    }
  }
}
