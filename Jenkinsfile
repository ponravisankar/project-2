pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }



        stage('Run Program') {
            steps {
                bat 'python3 app.py'
            }
        }
    }
}