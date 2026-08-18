pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                echo 'code has been checkout from  github'
            }
        }
        stage('Run python aplication'){
        steps{
            bat 'python app.py'
        }}
        stage('Environment Info') {
    steps {
        echo "Job Name: ${env.JOB_NAME}"
        echo "Build Number: ${env.BUILD_NUMBER}"
        echo "Workspace: ${env.WORKSPACE}"
        echo "Build URL: ${env.BUILD_URL}"
    }
}
        
    }
}
