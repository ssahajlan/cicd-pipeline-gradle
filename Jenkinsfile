pipeline {
  agent any
  stages {
    stage ('Checkout') { 
      steps {
        echo 'Source Code Checkoout Automation'
        git credentialsId: 'GituHub'
	          url: 'https://github.com/ssahajlan/cicd-pipeline-gradle'
      }  
    stage ('Build')  {
      steps {
        echo 'Running Build Automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/sampleapp.zip'
      }
    }
  }
}
