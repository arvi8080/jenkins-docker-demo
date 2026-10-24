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
                sh 'docker build -t jenkins-demo:${BUILD_NUMBER} .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'docker run --rm jenkins-demo:${BUILD_NUMBER}'
            }
        }
    }
}
