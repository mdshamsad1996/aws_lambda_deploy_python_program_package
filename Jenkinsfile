pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python3 --version'
            }
        }
        stage('stage 2- Install virtualenv'){
            steps {
                sh 'sudo -H pip install virtualenv'
            }
        }
        stage('stage 3- Creating Virtual Environment'){
            steps{
                sh ' python3 -m venv env'
            }
        }
        stage('stage 4- Activate Virtualenv'){
            steps {
                sh 'sudo -H . venv/bin/activate'
            }
        }
        stage('stage 5- Install dependency'){
            steps {
                sh 'sudo -H pip install -r requirements.txt -t ./'
            }
        }
        stage('stage 6- Run unit test case'){
            steps{
                sh 'python -m unittest tests/test_lambda_handler.py'
            }
        }
    }
}
