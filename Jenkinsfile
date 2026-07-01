pipeline {
    agent any

    stages {

        stage('Install Dependencies') {
            steps {
                bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" test.py'
            }
        }

        stage('Run Application') {
            steps {
                bat '"C:\\Users\\ponravisankar\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }
    }
}