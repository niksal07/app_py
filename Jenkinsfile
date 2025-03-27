pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/niksal07/app_py.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the application..."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }
    }
}
