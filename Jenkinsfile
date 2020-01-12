pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('Stage 1 - Check Python version') {
            steps {
                sh 'python3 --version'
            }
        }
        stage('stage 2- Creating Virtual Environment'){
            steps{
                sh 'virtualenv venv '
            }
        }
        stage('stage 3- Activate Virtualenv'){
            steps {
                sh ' . venv/bin/activate'
            }
        }
        stage('stage 4- Install dependency'){
            steps {
                sh 'sudo pip install -r requirements.txt -t ./'
            }
        }
        stage('stage 5- Run unit test case'){
            steps{
                sh 'python -m unittest tests/test_lambda_handler.py'
            }
        }
    }
}
