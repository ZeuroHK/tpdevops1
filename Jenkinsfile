pipeline {
agent any
stages {
stage('Clone Repository') {
steps {
checkout scm
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
script {
docker.image('my-app').inside {
sh 'node app.js &'
}
}
}
}
}
}