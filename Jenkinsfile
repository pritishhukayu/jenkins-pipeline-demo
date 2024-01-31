pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build and Deploy') {
            steps {
                echo 'Building and deploying the application...'
                // Create a directory in the Jenkins workspace
                sh 'mkdir -p ./deploy'
                // Example: Deploying to a web server
                sh 'cp index.html ./deploy/'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed. Check the logs for details.'
        }
    }
}
