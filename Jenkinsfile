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
                
                // Create the destination directory
                sh 'sudo mkdir -p /var/www/html/'
                
                // Copy the file to the destination directory
                sh 'sudo cp index.html /var/www/html/'
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
