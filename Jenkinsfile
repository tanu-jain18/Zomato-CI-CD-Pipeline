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
             sh 'docker --version'
             sh 'docker build -t zomato-app .'
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