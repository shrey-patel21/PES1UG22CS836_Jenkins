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
                    // Compile the .cpp file using g++
                    sh 'g++ main2.cpp -o output'

                    // Build the project (assuming 'YOUR_SRN-1' is the correct build command)
                    sh 'PES1UG22CS836-1'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file
                    sh './output'
                }
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
