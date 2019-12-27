pipeline {
    agent any
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python --version'
            }
        }
        stage('stage 2- run unit test'){
            steps{
                sh 'python -m unittest tests/test_lambda_handler.py'
            }
        }
    }
}