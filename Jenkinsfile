pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/niksal07/app_py.git'
            }
        }

        stage('Test') {
            steps {
                sh '''
                    python3 -m venv venv
                    source venv/bin/activate
                    pip3 install flask
                    python3 app.py
                '''
            }
        }
    }
}
