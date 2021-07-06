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
            archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
        }
}