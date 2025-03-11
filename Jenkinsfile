pipeline {
    agent any // Runs on any available Jenkins agent

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec hello.cpp' // Compile the C++ program
            }
        }

        stage('Test') {
            steps {
                sh './hello_exec' // Run the compiled C++ program
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...' // Dummy deploy step
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Please check errors in the logs.'
        }
    }
}
