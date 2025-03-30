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
                    . venv/bin/activate 
                    pip3 install --upgrade pip
                    pip3 install flask
                    timeout 300 python3 app.py  # Run for 5 minutes, then stop
                '''
            }
        }
    }
}
