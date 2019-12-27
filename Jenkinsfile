pipeline {
    agent any
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python --version'
            }
        }
        stage('Stage 2 - Run lambda_handler') {
            steps {
                sh 'python src/lambda_handler.py'
            }
        }
        stage('stage 3- run unit test'){
            steps{
                sh 'python -m unittest tests/test_lambda_handler.py'
            }
        }
    }
}