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
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Program') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}