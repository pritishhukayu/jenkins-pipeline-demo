pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out the code from the Git repository
                checkout scm
            }
        }

        stage('Build and Deploy') {
            steps {
                echo 'Building and deploying the application...'
                // Create the target directory if it doesn't exist
                sh 'sudo mkdir -p /var/www/html/'
                // Example: Deploying to a web server
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
