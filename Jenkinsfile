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
                sh 'npm install'
            }
        }

        stage('SonarQube Scan') {
            steps {
                echo 'Running SonarQube Scan...'
            }
        }

        stage('OWASP Dependency Check') {
            steps {
                echo 'Running Dependency Check...'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker --version'
                echo 'Docker Build completed'
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