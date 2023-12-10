pipeline {
    agent { docker { image 'python:3.7.2' } }
    stages {
        stage('build') {
            steps {
                sh 'chmod 777 ./local'
                sh 'pip3 install  flask --user'
            }
        }
        stage('test') {
            steps {
                sh 'python test.py'
            }
        }
    }
}
