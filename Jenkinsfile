pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/cleberleao/oficina-spring-boot.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t oficina-spring .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8081:8081 oficina-spring --name oficina-spring'
            }
        }
    }
}