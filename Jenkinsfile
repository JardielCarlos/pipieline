pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'pip install --user flask'
            }
        }
        stage('test') {
            steps {
                sh 'python test.py'
            }
        }
    }
}