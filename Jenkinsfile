pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps { checkout scm }
        }
        stage('Build') {
            steps { bat 'python app.py' }
        }
        stage('Test') {
            steps { bat 'python -c "import test_app; test_app.test_add(); print(\'Tests Passed!\')"' }
        }
    }
}
