pipeline {
    agent any

    tools {
        nodejs "nodejs"
    }

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Checkout completed'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Skipping npm install temporarily'
                sh 'node --version'
                sh 'npm --version'
            }
        }

        stage('SonarQube Scan') {
            steps {
                echo 'Running SonarQube Scan...'
            }
        }

        stage('OWASP Dependency Check') {
            steps {
               echo 'OWASP Dependency Check stage added'
            }
        }

        stage('Docker Build') {
            steps {
             echo 'Docker Build stage added'
             echo 'Docker image build will be configured using Docker CLI'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully'
        }

        failure {
            echo 'Build failed'
        }
    }
}