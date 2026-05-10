pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/ankitjha100/mvnsel.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run Jar') {
            steps {
                bat 'java -jar target/mvnsel-1.0-SNAPSHOT.jar'
            }
        }
    }
}
