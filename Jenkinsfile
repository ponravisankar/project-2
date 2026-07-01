pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                dir('python-app') {
                    bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
                }
            }
        }

        stage('Run Tests') {
            steps {
                dir('python-app') {
                    bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" test.py'
                }
            }
        }

        stage('Run Application') {
            steps {
                dir('python-app') {
                    bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
                }
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