pipeline {
agent any
stages {
stage('Clone') {
steps {
git 'https://github.com/ankitjha100/mvnsel.git'
}
}
stage('Build') {
steps {
sh 'mvn clean compile'
}
}
stage('Test Automation') {
steps {
sh 'mvn test'
}
}
}
}
