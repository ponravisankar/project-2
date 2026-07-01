
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from your repository
                git url:'https://github.com/ponravisankar/project-2.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Use Windows batch command to install requirements
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Run your test.py file
                bat 'python test.py'
            }
        }

        stage('Run Application') {
            steps {
                // Execute the main app.py file
                bat 'python app.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check logs.'
        }
    }
}