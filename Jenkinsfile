pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ZeuroHK/tpdevops1.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-app')
                }
            }
        }
        stage('Run Docker Container') {
    steps {
        bat 'docker run -d -p 3000:3000 my-app'
    }
}
    }
}