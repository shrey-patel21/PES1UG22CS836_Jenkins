pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello_exec'
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
