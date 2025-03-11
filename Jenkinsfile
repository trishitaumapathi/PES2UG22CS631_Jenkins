pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Compiling C++ code..."
                    sh 'g++ -o PES2UG22CS631-1 hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Running the compiled program..."
                    sh './nonexistent-binary'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                    sh 'echo "Deployment successful"'
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

