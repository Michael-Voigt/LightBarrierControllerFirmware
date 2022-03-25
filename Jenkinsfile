// After a new Jenkins build, a new Software Version has to be created out of the ECTR 
// on the build via context menu 'Transfer Build' 
// In addition to the new Software Version, a new Version of the Software Document is created
// and the all artifact will be uploaded to the new Version of the Software Document
//
// Therefore, no stage 'upload to SAP' is required

pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat 'mvn package'
            }
        }
        stage('upload to SAP') {
            steps {
                echo 'Upload to SAP'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'target/*.jar, config/*.*', fingerprint: true
        }
    }
}