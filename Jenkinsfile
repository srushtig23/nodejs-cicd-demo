pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/srushtig23/nodejs-cicd-demo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t nodejs-cicd-demo .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run -d -p 3000:3000 nodejs-cicd-demo'
            }
        }
    }
}
