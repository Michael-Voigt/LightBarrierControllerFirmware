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
}