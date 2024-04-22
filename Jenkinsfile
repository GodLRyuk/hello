pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    docker.build('webapp:latest')
                }
            }
        }

        stage('Test') {
            steps {
                // Run automated tests (placeholder)
                sh 'echo "Running tests..."'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy using Docker Compose
                    sh 'docker-compose up -d'
                }
            }
        }
    }

    post {
        always {
            // Cleanup steps, if needed
            script {
                docker.image('webapp:latest').remove()
            }
        }
    }
}
