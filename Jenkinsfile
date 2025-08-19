pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t react-landing-page .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker rm -f react-landing || true'
                sh 'docker run -d -p 8070:80 --name react-landing react-landing-page'
            }
        }
    }
}
