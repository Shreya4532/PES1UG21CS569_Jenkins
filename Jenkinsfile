pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Move to the 'main' directory
                dir('main') {
                    sh 'g++ hello.cpp -o hello'
                }
            }
        }
        stage('Test') {
            steps {
                // Move to the 'main' directory
                dir('main') {
                    sh './hello' 
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
