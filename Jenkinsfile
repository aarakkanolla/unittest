pipeline {
    agent any
    environment {
     PATH = '/home/tom/bin:/home/tom/.local/bin:/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games:/snap/bin:/usr/local/jdk/bin:/usr/local/maven/bin:/usr/local/apache-ant-1.10.5/bin' 
}

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
        stage('Archive') {
            steps{
               sh 'archiveArtifacts '**/*.jar'
            }
        }
        stage('Publish_reports') {
            steps {
                echo 'convert to html'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp target/*.jar /tmp'
            }
        }
    }
}
