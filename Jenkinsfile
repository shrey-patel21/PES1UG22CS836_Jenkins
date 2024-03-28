pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name:'*/main']],
                          userRemoteConfigs: [url:'https://github.com/shrey-patel21/PES1UG22CS836_Jenkins.git']])
            }
        }
        stage('Build') {
            steps {
                script {
                    build job: 'PES1UG22CS836-1' // Assuming 'PES1UG22CS836-1' is a valid Jenkins job name
                    sh 'g++ main2.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                sh './output'
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
            error 'Pipeline failed'
        }
    }
}
