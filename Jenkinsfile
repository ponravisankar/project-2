pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Packages') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Program') {
            steps {
                bat 'python app.py'
            }
        }

    }
}