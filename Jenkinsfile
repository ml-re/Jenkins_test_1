pipeline {
    agent { docker { image 'python:3.12.1-alpine3.19' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
    post {
        always {
            echo "Finished somehow"
            mail to: "mariusz.lesniewski@gmail.com", subject: "Jenkins test message from ${currentBuild.fullDisplayName}", body: "The ${env.BUILD_URL} somehow finished"
        }
        success {
            echo "Finished successfully"
        }
    }
}
