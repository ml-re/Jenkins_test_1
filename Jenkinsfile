pipeline {
    agent { docker { image 'python:3.12.1-alpine3.19' } }
    stages {
        stage('build') {
            steps {
                input "Jak to działa?"
                sh 'python --version'
            }
        }
    }
    post {
        always {
            echo "Finished somehow"
        }
        success {
            echo "Finished successfully"
        }
    }
}
