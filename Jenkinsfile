pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/my-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f my-app || true'
                sh 'docker run -d -p 80:80 --name my-app my-app'
            }
        }
    }
}
