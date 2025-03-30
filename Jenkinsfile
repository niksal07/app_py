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
                    nohup python3 app.py & 
                    sleep 300  # Keep it running for 5 mins
                    pkill -f "python3 app.py"  # Stop Flask after 5 mins
                '''
            }
        }
    }
}
