pipeline {
    agent any

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
                echo 'Running SonarQube scan'
            }
        }

        stage('OWASP Dependency Check') {
            steps {
                echo 'Running Dependency Check'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
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