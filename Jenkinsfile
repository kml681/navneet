pipeline {
    agent any

    environment {
        APP_NAME = "MyApp"
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/example/myapp.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo "Building ${APP_NAME}"
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh './deploy.sh'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }

        success {
            echo 'Build succeeded!'
        }

        failure {
            echo 'Build failed!'
        }
    }
}