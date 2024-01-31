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
                // Your build and deployment steps go here
                echo 'Building and deploying the application...'
                // Example: Deploying to a web server
                sh 'cp index.html /var/www/html/'
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
