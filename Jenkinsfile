pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
                sh './script.sh'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running code analysis...'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running security scan...'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production environment...'
            }
        }
    }

    post {
        always {
            mail to: 'developer@example.com',
                 subject: "Pipeline Result: ${currentBuild.currentResult}",
                 body: "Check the pipeline logs and build results."
        }
    }
}
