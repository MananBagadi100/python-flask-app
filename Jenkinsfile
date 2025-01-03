pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Install dependencies
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                // Run unit tests
                sh 'python -m unittest discover'
            }
        }
        stage('Deploy') {
            steps {
                // Mock deployment by copying files
                sh '''
                mkdir -p /path/to/deployment/directory
                cp -r * /path/to/deployment/directory/
                '''
            }
        }
    }
}
