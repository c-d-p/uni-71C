pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *') // no webhook, just polling every minute
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build and package the code. Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Run unit and integration tests. Tools: JUnit and Selenium'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Check code quality. Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Scan for vulnerabilities. Tool: Snyk'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to a staging server. Tool: AWS CLI and EC2'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Test the staging application. Tool: Postman/Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy to production. Tool: AWS CLI and EC2'
            }
        }
    }
}