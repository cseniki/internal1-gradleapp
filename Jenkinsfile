pipeline {
agent any 
tools {
gradle 'gradle' 
jdk 'java'
}
stages {
stage('Checkout') {
steps {
git branch: 'main', url: 'https://github.com/cseniki/internal1-gradleapp.git'
}
}
stage('Build') {
steps {
sh 'gradle build' 
}
}
stage('Test') {
steps {
sh 'gradle test' 
}
}
stage('Run Application') {
steps {
sh 'gradle run'
}
}
}
post {
success {
echo 'Build and deployment successful!'
}
failure {
echo 'Build failed!'
}
}
}
