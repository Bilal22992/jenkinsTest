pipeline {
    agent any
    stages {
        stage('Testing the Bridge') {
            steps {
                // Ensure the code is there
                sh 'ls -la'
            }
        }
        stage('Deploying Nginx') {
            steps {
                // Remove the old one if it exists
                sh 'docker rm -f test-bridge || true'
                // Run the new one just like your original command
                sh 'docker run -d --name test-bridge -p 81:80 nginx:latest'
            }
        }
    }
}
