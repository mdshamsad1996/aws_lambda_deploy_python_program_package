pipeline {
    agent any
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python3 --version'
            }
        }
        stage('stage 2- Install virtualenv'){
            steps {
                sh 'sudo pip install virtualenv'
            }
        }
        stage('stage 3- Activate Virtualenv'){
            steps {
                sh 'sudo source env/bin/activate'
            }
        }
        stage('stage 4- Install dependency'){
            steps {
                sh 'pip install -r requirements.txt -t ./'
            }
        }
        stage('stage 5- Run unit test case'){
            steps{
                sh 'python -m unittest tests/test_lambda_handler.py'
            }
        }
    }
}