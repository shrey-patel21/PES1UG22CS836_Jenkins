pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output '
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
             echo 'deploy'  
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
