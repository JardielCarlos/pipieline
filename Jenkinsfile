pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'chmod -R 777 /.local'
                sh 'pip install --upgrade --user pip'
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
