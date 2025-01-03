pipeline {
    agent any

    stages {
        stage('Setup Virtual Environment') {
            steps {
                sh '''
                python3 -m venv venv
                source venv/bin/activate
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                source venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                source venv/bin/activate
                python -m unittest discover
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                source venv/bin/activate
                mkdir -p /path/to/deployment/directory
                cp -r * /path/to/deployment/directory/
                '''
            }
        }
    }
}
