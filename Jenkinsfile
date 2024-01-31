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

                // Provide your sudo password using the echo command
                def sudoPassword = SerAdmin#637

                // Use sudo -S to read the password from stdin
                sh "echo ${sudoPassword} | sudo -S mkdir -p /var/www/html/"

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
