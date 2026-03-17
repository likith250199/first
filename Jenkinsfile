pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/likith250199/first.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 devops-app'
            }
        }
    }
}
