pipeline {
    agent any

    stages {

        stage('Linux Check') {
            steps {
                sh 'whoami'
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-demo:1.0 .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker run --rm jenkins-demo:1.0'
            }
        }
    }
}
