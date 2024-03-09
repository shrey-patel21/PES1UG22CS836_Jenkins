pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Perform build steps here
                    echo 'Building...'
                    // Example: sh 'make'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Perform testing steps here
                    echo 'Testing...'
                    // Example: sh 'make test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Perform deployment steps here
                    echo 'Deploying...'
                    // Example: sh 'make deploy'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
