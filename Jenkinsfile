pipeline {
    agent {
        docker {
            image 'ubuntu:22.04'
            args '-u root'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Running inside Docker container"'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                sh 'cat hello.txt'
            }
        }
    }
}
