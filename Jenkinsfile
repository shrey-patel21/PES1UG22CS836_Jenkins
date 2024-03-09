pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello.cpp'
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
