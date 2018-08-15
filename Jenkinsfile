pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh 'ant test'
            }
        }
        stage('Build') {
            steps {
                sh 'ant build'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp dist/*.war/tmp'
            }
        }
    }
}
