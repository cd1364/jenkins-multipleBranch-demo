pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out source code from branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests on branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Build') {
            steps {
                echo "Building application for branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application from branch: ${env.BRANCH_NAME}"
            }
        }
    }

    post {
        always {
            echo "Pipeline finished for branch: ${env.BRANCH_NAME}"
        }
        success {
            echo "Pipeline succeeded for branch: ${env.BRANCH_NAME}"
        }
        failure {
            echo "Pipeline failed for branch: ${env.BRANCH_NAME}"
        }
    }
}
