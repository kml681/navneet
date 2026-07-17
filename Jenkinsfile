pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Stage Started'
                sh 'hostname'
            }
        }

        stage('Test') {
            steps {
                echo 'Test Stage Started'
                sh 'uptime'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage Started'
                sh 'date'
            }
        }
    }

    post {
        success {
            echo 'Pipeline Completed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }
}