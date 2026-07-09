pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Run Program') {
            steps {
                echo 'Running Python Program...'
                bat 'python3 app.py'
            }
        }

    }

    post {
        success {
            echo Build completed successfully!
        }

        failure {
            echo Build failed!
        }
    }
}