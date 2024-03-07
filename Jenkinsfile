pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compiling the hello.cpp file
                // The output binary will be named as `app`
                sh 'g++ -o app hello.cpp'
            }
        }
        
        stage('Test') {
            steps {
                // Printing the output of the compiled hello.cpp file
                // This assumes that running `./app` will produce some output that can be considered a test
                sh './app'
            }
        }
        
        stage('Deploy') {
            steps {
                // Add your deploy steps here
                // This example does not include specific deployment steps as it can vary greatly depending on the target environment
                echo 'Deploying application...'
            }
        }
    }

    post {
        // This block executes after the pipeline run
        failure {
            // If any of the stages fail, this message will be printed
            echo 'Pipeline failed!'
        }
    }
}
