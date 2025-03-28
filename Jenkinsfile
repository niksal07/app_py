pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/niksal07/app_py.git'
            }
        }

	stage('Install Dependencies') {
	    steps {
        	sh 'pip3 install flask'
    	    }	
	}

        stage('Build') {
            steps {
                sh 'echo "Building Application..."'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 app.py'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying Application..."'
            }
        }
    }
}

