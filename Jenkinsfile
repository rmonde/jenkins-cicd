pipeline {
    agent any

    stages {
        stage('Build'){
            steps {
                bat 'F:\Study\Jenkins\apache-maven-3.6.0-bin\apache-maven-3.6.0\bin\mvn clean package'
            }
        post {
            success {
                echo 'Now Archiving...'
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }
     }
    }
}