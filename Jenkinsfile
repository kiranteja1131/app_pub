pipeline {
    agent any

    environment {
        APP_NAME = 'MyPythonApp'
        ENVIRONMENT = 'development'
    }

    stages {
        stage('Environment Info') {
            steps {
                echo "Application: ${env.APP_NAME}"
                echo "Environment: ${env.ENVIRONMENT}"
                echo "Build Number: ${env.BUILD_NUMBER}"
            }
        }

        stage('Run Python App') {
            steps {
                bat 'python app.py'
            }
        }
    }
    post {
    always {
        echo 'Pipeline execution completed'
    }

    success {
        echo 'Pipeline completed successfully!'
    }

    failure {
        echo 'Pipeline failed!'
    }
}
}