
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'docker build -t labskraft-app .'
            }
        }

        stage('Report') {
            steps {
                sh '''
                echo GIT_CLONE=SUCCESS > evaluation_report.txt
                echo DOCKER_BUILD=SUCCESS >> evaluation_report.txt
                echo FINAL_STATUS=SUCCESS >> evaluation_report.txt
                '''
            }
        }
    }
}
