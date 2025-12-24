pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build inside Docker') {
            steps {
                bat '''
                docker run --rm ^
                  -v "%cd%":/workspace ^
                  -w /workspace ^
                  ubuntu:22.04 ^
                  bash -c "echo Running inside Docker && ls -la"
                '''
            }
        }

        stage('Test inside Docker') {
            steps {
                bat '''
                docker run --rm ^
                  -v "%cd%":/workspace ^
                  -w /workspace ^
                  ubuntu:22.04 ^
                  bash -c "cat hello.txt"
                '''
            }
        }
    }
}
