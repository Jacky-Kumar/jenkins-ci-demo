pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
                echo 'Code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building project'
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                bat 'type hello.txt'
            }
        }
    }
}
