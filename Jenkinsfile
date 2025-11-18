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
docker.build('tpdevops1')
}
}
}
stage('Run Docker Container') {
steps {
script {
docker.image('tpdevops1').inside {
sh 'node app.js &'
}
}
}
}
}
}